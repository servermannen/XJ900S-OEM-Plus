# RESEARCH-0004: rusEFI dual-bank short-term fuel trim

**Purpose:** Record the static and dynamic evidence for configurable dual-bank
short-term fuel trim in rusEFI without selecting an ECU, lambda-sensor layout,
exhaust configuration, or final fuel-control architecture.

**Document status: Review**

**Status: Confirmed**

**Review: Technically Reviewed**

The `Confirmed` status and completed technical review apply only to the
demonstrated rusEFI software behavior at the pinned upstream revision. They do
not confirm XJ900S hardware suitability or accept an implementation.

## 1. Purpose

This record preserves the completed static source-code review and host-side
unit-test evidence for rusEFI dual-bank short-term fuel trim (STFT). It records
what the pinned software revision demonstrated, the configuration constraints
under which it was demonstrated, and the evidence still required before the
capability can inform an XJ900S OEM+ architecture decision.

## 2. Scope and boundaries

### Included

- Static analysis of dual-bank STFT behavior in the pinned rusEFI revision.
- A host-side unit test of four-cylinder sequential injection with two
  independently corrected cylinder banks.
- Physical-cylinder bank lookup, injection-mass grouping, calculated
  host-test injector duration, and sequential scheduler output selection.
- Immediate behavior after invalidating one lambda input.

### Excluded

- Acceptance of rusEFI or any rusEFI ECU hardware.
- Acceptance of a lambda-sensor count, location, controller, or wiring
  interface.
- Acceptance of an XJ900S exhaust layout or fuel-control architecture.
- Injector sizing, duty-cycle analysis, electrical-driver validation, fuel
  pressure, calibration, emissions, or motorcycle operation.
- Hardware, bench-system, engine, or road validation.
- Batch, simultaneous, single-point, duty-cycle protection, or
  frozen-sensor-detection testing.

The unit test used firing order `1-3-4-2` solely as a rusEFI software-test
configuration. It is not an XJ900S firing-order claim. Existing
[RESEARCH-0003](RESEARCH-0003-trigger-and-synchronization-strategy.md) records
a different manual-stated firing order for the 1995 4KM1 source, with
applicability to the project-recorded 1997 motorcycle still Unverified.

## 3. Upstream revision

| Item | Recorded evidence |
| --- | --- |
| Upstream repository | [rusefi/rusefi](https://github.com/rusefi/rusefi) |
| Reviewed and tested revision | [`942110a93c0cb8b3ca6caf77a0b56fba9c3065c2`](https://github.com/rusefi/rusefi/commit/942110a93c0cb8b3ca6caf77a0b56fba9c3065c2) |
| Upstream branch context | `master` |
| Test modification | `unit_tests/tests/test_stft.cpp` |
| Test name | `ClosedLoopFuel.DualBankSequentialPhysicalCylinderMapping` |
| Test-result date | 2026-08-07 |
| Test-result classification | PASS |

The unit-test case was added only in an isolated disposable checkout based on
the recorded revision. It was not committed or pushed to the upstream
repository, and production firmware code was not modified.

### Preserved dynamic-test evidence

| Item | Evidence |
| --- | --- |
| Patch | [RESEARCH-0004-rusefi-dual-bank-stft-test.patch](evidence/RESEARCH-0004-rusefi-dual-bank-stft-test.patch) |
| SHA-256 | `A6A802341EB0994AE8B9D59ED0A9A525E6EDEF7C809175DAAD42448B92B893DB` |
| Upstream base revision | `942110a93c0cb8b3ca6caf77a0b56fba9c3065c2` |
| Test file | `unit_tests/tests/test_stft.cpp` |
| Test name | `ClosedLoopFuel.DualBankSequentialPhysicalCylinderMapping` |
| Apply check | `PASS` — `git apply --check` completed in a clean disposable checkout at the upstream base revision. |

The patch is preserved for reproducibility. It was not accepted or merged into
upstream rusEFI.

## 4. Static-analysis result

Static-review conclusion: **Supported with configuration constraints.**

At the pinned revision, the reviewed implementation supports two independent
STFT corrections and selects the correction through the configured physical
cylinder's `cylinderBankSelect` entry. Sequential firing-order position does
not replace the physical-cylinder lookup. Correct behavior therefore depends
on a configuration whose bank assignments match the intended physical
cylinders and whose lambda inputs represent the corresponding exhaust banks.

The static review also found that making a lambda input invalid stops learning
for that bank while leaving its previously learned correction available; no
subsequent decay toward unity was identified in the reviewed path. That
no-decay conclusion is static source-code evidence, not the result of a
long-duration dynamic test.

### Immutable static evidence trace

The following links preserve the reviewed executable-code trace at the pinned
revision. They describe rusEFI behavior only and do not accept an XJ900S
hardware, sensor, or exhaust architecture.

| Finding | Pinned source evidence |
| --- | --- |
| Two fuel-trim banks | `firmware/integration/rusefi_config_shared.txt` — `FT_BANK_COUNT` is defined as `2` ([lines 29-30](https://github.com/rusefi/rusefi/blob/942110a93c0cb8b3ca6caf77a0b56fba9c3065c2/firmware/integration/rusefi_config_shared.txt#L29-L30)). |
| Lambda sensor routing | `firmware/controllers/math/closed_loop_fuel.cpp` — `ShortTermFuelTrim::getSensorForBankIndex` maps bank `0` to `Lambda1` and bank `1` to `Lambda2` ([lines 17-23](https://github.com/rusefi/rusefi/blob/942110a93c0cb8b3ca6caf77a0b56fba9c3065c2/firmware/controllers/math/closed_loop_fuel.cpp#L17-L23)). |
| Configurable bank selection | `firmware/controllers/generated/engine_configuration_generated_structures_uaefi.h` — the `cylinderBankSelect[MAX_CYLINDER_COUNT]` configuration field selects the fuel-correction bank ([lines 5108-5111](https://github.com/rusefi/rusefi/blob/942110a93c0cb8b3ca6caf77a0b56fba9c3065c2/firmware/controllers/generated/engine_configuration_generated_structures_uaefi.h#L5108-L5111)). |
| Base/default assignment | `firmware/controllers/algo/defaults/default_base_engine.cpp` — base defaults set every `cylinderBankSelect[i]` to bank `0` ([lines 290-294](https://github.com/rusefi/rusefi/blob/942110a93c0cb8b3ca6caf77a0b56fba9c3065c2/firmware/controllers/algo/defaults/default_base_engine.cpp#L290-L294)); `setLeftRightBanksNeedBetterName` provides an alternating assignment helper ([lines 95-101](https://github.com/rusefi/rusefi/blob/942110a93c0cb8b3ca6caf77a0b56fba9c3065c2/firmware/controllers/algo/defaults/default_base_engine.cpp#L95-L101)). |
| Physical-cylinder STFT-bank lookup | `firmware/controllers/algo/engine2.cpp` — `engineConfiguration->cylinderBankSelect[cylinderIndex]` selects `bankIndex` for each physical cylinder ([lines 244-249](https://github.com/rusefi/rusefi/blob/942110a93c0cb8b3ca6caf77a0b56fba9c3065c2/firmware/controllers/algo/engine2.cpp#L244-L249)). |
| STFT applied to physical-cylinder injection mass | `firmware/controllers/algo/engine2.cpp` — `clResult.banks[bankIndex]` becomes `bankTrim` and is multiplied into `engineState.injectionMass[cylinderIndex]` ([lines 248-256](https://github.com/rusefi/rusefi/blob/942110a93c0cb8b3ca6caf77a0b56fba9c3065c2/firmware/controllers/algo/engine2.cpp#L248-L256)). |
| Firing-order position to physical-cylinder mapping | `firmware/controllers/algo/engine_cylinder.cpp` — `EngineCylinders::updateCylinders` converts each firing-order position through `getCylinderNumberAtIndex(i)` before updating the physical cylinder ([lines 40-52](https://github.com/rusefi/rusefi/blob/942110a93c0cb8b3ca6caf77a0b56fba9c3065c2/firmware/controllers/algo/engine_cylinder.cpp#L40-L52)); `firmware/controllers/math/firing_order.cpp` returns the physical cylinder number ([lines 246-270](https://github.com/rusefi/rusefi/blob/942110a93c0cb8b3ca6caf77a0b56fba9c3065c2/firmware/controllers/math/firing_order.cpp#L246-L270)). |
| Physical injector-output selection | `firmware/controllers/engine_cycle/fuel_schedule.cpp` — sequential or batch scheduling derives `injectorIndex` from `getCylinderNumberAtIndex(ownIndex)` and selects `enginePins.injectors[injectorIndex]` ([lines 155-185](https://github.com/rusefi/rusefi/blob/942110a93c0cb8b3ca6caf77a0b56fba9c3065c2/firmware/controllers/engine_cycle/fuel_schedule.cpp#L155-L185)). |
| Invalid lambda pauses learning while stored adjustment remains applied | `firmware/controllers/math/closed_loop_fuel.cpp` — invalid AFR returns the paused learning state without reset ([lines 81-92](https://github.com/rusefi/rusefi/blob/942110a93c0cb8b3ca6caf77a0b56fba9c3065c2/firmware/controllers/math/closed_loop_fuel.cpp#L81-L92)); `cell.update()` runs only when learning is enabled, while `cell.getAdjustment()` is assigned to each result bank ([lines 127-154](https://github.com/rusefi/rusefi/blob/942110a93c0cb8b3ca6caf77a0b56fba9c3065c2/firmware/controllers/math/closed_loop_fuel.cpp#L127-L154)). |
| No decay logic in the reviewed STFT cell path | `firmware/controllers/math/closed_loop_fuel.cpp` — the reviewed result path conditionally calls `cell.update()` and returns `cell.getAdjustment()`; it contains no decay or reset call in that path ([lines 127-154](https://github.com/rusefi/rusefi/blob/942110a93c0cb8b3ca6caf77a0b56fba9c3065c2/firmware/controllers/math/closed_loop_fuel.cpp#L127-L154)). |

This analysis does not establish that an XJ900S exhaust or sensor arrangement
can provide bank-representative measurements.

## 5. Dynamic-test configuration

The host-side unit test configured:

- four cylinders;
- firing order `1-3-4-2`;
- sequential injection;
- `cylinderBankSelect = {0, 0, 1, 1}` for physical cylinders 1 through 4;
- STFT enabled;
- Lambda1 set to `1.100` and Lambda2 set to `0.900` against a lambda target of
  `1.000`;
- `Clt` test-harness sensor input above the configured minimum threshold,
  without implying an XJ900S coolant-temperature sensor requirement;
- startup delay satisfied;
- DFCO disabled and no recent DFCO state;
- no recent acceleration enrichment;
- no active fuel cuts; and
- injection permitted by the test engine state.

The test supplied Lambda1 and Lambda2 through the sensor interface and invoked
the real `ShortTermFuelTrim` integrators through periodic engine callbacks. It
did not inject precomputed STFT correction values into the final fueling
calculation.

## 6. Dynamic-test results

**Result: PASS**

The two lambda inputs produced distinct corrections:

| Observed item | Value | Evidence status |
| --- | ---: | --- |
| Lambda1 | 1.100 | Confirmed in the host test |
| Lambda2 | 0.900 | Confirmed in the host test |
| STFT bank 0 | 1.050000 | Confirmed in the host test |
| STFT bank 1 | 0.950000 | Confirmed in the host test |

### Exact build command

The command was run from `unit_tests/` in the disposable checkout after the
portable build dependencies had been prepared:

```powershell
$jdk21 = (Resolve-Path '..\.toolchain\jdk21\jdk-21.0.12+8').Path
$w64bin = (Resolve-Path '..\.toolchain\w64devkit\bin').Path
$env:JAVA_HOME = $jdk21
$env:GRADLE_USER_HOME = (Resolve-Path '..\.toolchain\gradle-home').Path
$env:Path = $w64bin + ';' + $jdk21 + '\bin;C:\Program Files\Git\bin;C:\Program Files\Git\cmd;' + $env:Path
make -j12 FLOCK=true 'RUSEFI_OPT=-Werror -Werror=stringop-truncation -Werror=shadow -Wno-error=sign-compare -Wno-error=overloaded-virtual -Wno-error=unused-parameter -Wno-delete-non-abstract-non-virtual-dtor -Wno-error=maybe-uninitialized'
```

The final warning demotion accommodated a GCC 16 warning in pre-existing unit
test mock code. It did not require a production source-code change.

### Exact test command

```powershell
& .\build\rusefi_test.exe '--gtest_filter=*ClosedLoopFuel*'
```

### Complete PASS summary

File-writing diagnostics and unrelated build chatter are omitted. The complete
pass/fail summary and the evidence lines emitted by the new test were:

```text
Note: Google Test filter = *ClosedLoopFuel*
[==========] Running 4 tests from 2 test suites.
[ RUN      ] ClosedLoopFuelCell.AdjustRate
[       OK ] ClosedLoopFuelCell.AdjustRate (0 ms)
[ RUN      ] ClosedLoopFuel.CellSelection
[       OK ] ClosedLoopFuel.CellSelection (0 ms)
[ RUN      ] ClosedLoopFuel.afrLimits
[       OK ] ClosedLoopFuel.afrLimits (4 ms)
[ RUN      ] ClosedLoopFuel.DualBankSequentialPhysicalCylinderMapping
DualBankSTFT lambda1=1.100 lambda2=0.900 bank0=1.050000 bank1=0.950000 mass=[0.07500001,0.07500001,0.06785715,0.06785715] duration_ms=[31.250004,31.250004,28.273809,28.273809] firing_order_outputs=[1,3,4,2]
DualBankSTFT invalid_lambda1 bank0_retained=1.050000 cylinder1_mass_retained=0.07500001
[       OK ] ClosedLoopFuel.DualBankSequentialPhysicalCylinderMapping (5 ms)
[==========] 4 tests from 2 test suites ran. (10 ms total)
[  PASSED  ] 4 tests.
Total tests execution time: 0.014 s
DONE returning 0
```

## 7. Physical cylinder-to-bank mapping

| Physical cylinder | Configured bank | Applied STFT | Injection mass, host-test value | Calculated duration, host test |
| ---: | ---: | ---: | ---: | ---: |
| 1 | 0 | 1.050000 | 0.07500001 | 31.250004 ms |
| 2 | 0 | 1.050000 | 0.07500001 | 31.250004 ms |
| 3 | 1 | 0.950000 | 0.06785715 | 28.273809 ms |
| 4 | 1 | 0.950000 | 0.06785715 | 28.273809 ms |

The equal values within each configured bank and the distinguishable values
between banks confirm the expected two-bank grouping in the host test.

The duration values are outputs of this host-test injector model only. They are
not injector-sizing values, duty-cycle evidence, electrical-driver
requirements, or hardware requirements for the XJ900S.

## 8. Sequential scheduler verification

| Firing-order position | Physical injector output | Physical-cylinder bank | Host-test injection mass | Calculated duration |
| ---: | ---: | ---: | ---: | ---: |
| 1 | 1 | 0 | 0.07500001 | 31.250004 ms |
| 2 | 3 | 1 | 0.06785715 | 28.273809 ms |
| 3 | 4 | 1 | 0.06785715 | 28.273809 ms |
| 4 | 2 | 0 | 0.07500001 | 31.250004 ms |

The observed sequential output order was `1-3-4-2`, and its bank sequence was
`0-1-1-0`. The test asserted that each firing-order event selected the
corresponding physical injector output and scheduled its close event using the
duration calculated from that physical cylinder's bank-corrected mass.

This demonstrates that changing firing-order position did not change the
physical-cylinder `cylinderBankSelect` lookup in the tested configuration.

## 9. Lambda failure observation

After bank 0 had learned a correction of `1.050000`, the test made Lambda1
invalid and invoked one additional periodic callback. The observed result was:

- bank-0 learning state changed to `stftDisabledAfrOurOfRange`;
- the previously learned bank-0 correction remained `1.050000`; and
- physical cylinder 1 injection mass remained `0.07500001`.

The dynamic test therefore confirms immediate correction retention for the one
tested callback after invalidation. It did not run a long-duration invalid
sensor scenario. The conclusion that the correction does not subsequently
decay toward unity comes from the static source-code review at the pinned
revision and shall not be represented as long-duration dynamic evidence.

## 10. Confirmed findings

**Status: Confirmed**

The following findings are confirmed only for rusEFI software at revision
`942110a93c0cb8b3ca6caf77a0b56fba9c3065c2` and the recorded host-test
configuration:

- Lambda1 and Lambda2 exercised separate real STFT integrators and produced
  distinct bank corrections.
- Physical cylinders 1 and 2 used bank 0, while physical cylinders 3 and 4
  used bank 1.
- Physical-cylinder injection masses preserved the expected bank grouping.
- Calculated host-test injector durations preserved the same bank grouping.
- The sequential scheduler selected physical injector outputs in the
  configured `1-3-4-2` firing order while retaining each physical cylinder's
  bank-corrected mass.
- Firing-order position did not replace or reorder the physical-cylinder bank
  lookup.
- Invalidating Lambda1 stopped bank-0 learning and retained the learned
  correction for the one dynamically tested callback.

These findings do not confirm an ECU, wideband controller, sensor, exhaust
layout, injector, wiring design, or motorcycle-level implementation.

## 11. Unverified XJ900S-specific items

**Status: Unverified**

- Actual exhaust gas routing through the original 4-2 system.
- Amount of cross-bank exhaust mixing.
- Final lambda-sensor locations.
- Hardware WBO/controller selection.
- rusEFI hardware/ECU selection.
- Behavior during loss of phase/cam synchronization.
- Whether runtime fallback changes sequential injection to batch or
  simultaneous.
- Suitability of retained STFT after lambda-sensor failure.
- Final injector sizing and duty-cycle margins.
- Frozen-but-plausible lambda detection.

## 12. Safety implications

Fuel control is safety-critical. The software behavior demonstrated here can
support further investigation, but it is not evidence that a dual-lambda
installation would measure or control the XJ900S correctly. Exhaust mixing,
sensor placement, controller diagnostics, stale or invalid data, phase loss,
fallback behavior, injector capacity, electrical integration, and safe-state
strategy can each change the safety meaning of the demonstrated capability.

Retention of a learned correction after an invalid lambda input may preserve
continuity, but it may also preserve a correction that is no longer suitable
for current operating conditions. No retained-correction failure strategy is
accepted by this record.

The host-test pulse durations shall not be used for injector procurement,
duty-cycle limits, driver design, calibration, or road-operation decisions.
Hardware implementation requires separate requirements, hazard analysis,
technical review, controlled bench evidence, and later motorcycle validation.

## 13. Remaining evidence gaps

- Direct inspection and mapping of the project motorcycle's exhaust paths and
  cross-bank mixing.
- Evidence that proposed lambda locations provide representative and
  sufficiently independent measurements under relevant conditions.
- Hardware wideband-controller and ECU electrical, diagnostic, environmental,
  and serviceability evidence.
- Dynamic behavior during loss and recovery of cam or phase synchronization,
  including whether injection mode changes.
- Long-duration invalid-lambda behavior and a defined strategy for retained
  correction, recovery, and driver notification.
- Frozen-but-plausible lambda detection and response.
- Separate tests for batch, simultaneous, single-point, and other fallback
  modes if an architecture later proposes them.
- Injector flow, fuel-pressure, dead-time, electrical-driver, transient,
  maximum-duration, and duty-cycle evidence using selected hardware.
- Safe-load bench evidence followed by controlled engine and motorcycle
  evidence within approved test scopes.

## 14. Next evidence-producing actions

1. Inspect and document the original 4-2 exhaust routing, junctions, and
   plausible cross-bank mixing paths on the project motorcycle.
2. Define candidate lambda-sensor locations only after the exhaust-path
   evidence exists, then evaluate whether each location can represent the
   intended cylinder bank.
3. Review and dynamically test rusEFI phase-loss, cam-loss, resynchronization,
   and injection-mode fallback behavior at an exactly pinned revision.
4. Define and test an invalid, disconnected, stale, and frozen-but-plausible
   lambda strategy, including retained-correction duration and recovery.
5. Evaluate candidate wideband controllers and rusEFI ECU hardware in separate
   component records against electrical, environmental, diagnostic,
   serviceability, and safety requirements.
6. Calculate and bench-verify injector sizing and duty-cycle margin only after
   fuel-pressure, flow, dead-time, engine-demand, and hardware inputs are
   evidenced.
7. Use safe loads to verify the selected complete hardware path before any
   installed fuel-control test.

These actions produce evidence; they do not pre-approve their candidate
components or architectures.

## 15. Conclusion

### Confirmed

**Status: Confirmed**

Current rusEFI at the pinned revision supports user-configurable dual-bank STFT
for a four-cylinder engine, including physical cylinders 1-2 assigned to
Lambda1/bank 0 and physical cylinders 3-4 assigned to Lambda2/bank 1, with
independent corrections preserved through sequential injector scheduling.

### Proposal

**Status: Proposal**

This capability is suitable for continued evaluation for XJ900S OEM+.

### Not accepted

**Status: Unverified**

The final dual-lambda XJ900S architecture remains open pending exhaust-path
verification, synchronization/fallback analysis, sensor-failure strategy, and
hardware validation.

## Change history

| Date | Change | Reason |
| --- | --- | --- |
| 2026-08-07 | Created the research record. | Preserve the pinned static-review and host-test evidence without accepting an XJ900S implementation. |

## Navigation

[Research index](README.md) | [RESEARCH-0001](RESEARCH-0001-engine-management-platform.md) | [RESEARCH-0002](RESEARCH-0002-level-1-io-and-trigger-requirements.md) | [RESEARCH-0003](RESEARCH-0003-trigger-and-synchronization-strategy.md) | [System requirements](../requirements/system-requirements.md) | [System architecture](../architecture/system-architecture.md) | [Test strategy](../testing/test-strategy.md) | [Documentation index](../INDEX.md)
