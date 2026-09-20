# Changelog

## 6.4.2 — 2026-09-20

- Adds strict version migrations for older piston Free sessions and measurements so records still present in storage can appear again. Raw samples, frozen parameters, and valid period readings are retained in the experiment group; obsolete fits and downstream calculations require recomputation. Unknown fields, future versions, and damaged evidence remain preserved and quarantined, with no relaxation of exact answer checks.
- Adds the missing @emnapi/runtime 1.11.3 peer required by an optional WASM build branch, resolving rejection by newer npm versions. A regression check covers all required peers; existing dependency versions, URLs, and integrity values are preserved.
- The Windows upgrade workflow installs locked dependencies before downloading or installing either app. Legacy probes are restricted to clean hosted Windows runners, verify the original file identity, and restart again after upgrade to confirm persistence. Ordinary local execution is rejected before launching an old app.
- Reviews links, version context, and identity information in new current documents; adds the missing architecture-composition index; and distinguishes historical candidates, releases, and incomplete checks. Archived plans and model scans are not reclassified as pending work or physical calibration.
- Retains the application ID, installer identity, user-data directory, and update repository, with the installer and complete update assets. Experiment behavior, state ownership, persistence, and exact answer checks match 6.4.1. Obsolete fits and downstream calculations from earlier piston versions still require recomputation.

## 6.4.1 — 2026-09-15

- Both methods support Real/Ideal experiment conditions and air/helium. Ideal presets remove modeled environmental, observation, and loss disturbances while retaining manual operation, processing, and calculation. Incorrect operation still has physical consequences; Ideal provides diagnostics without numerical scores.
- First use records familiarity with each method and unlocks Demo, Guide, and Free in sequence where learning is needed. Demo and unfinished Guide sessions do not become Free experiments. Completed guides remain reviewable, and Free data survives mode switching until a full reset.
- Guided selections require at least two reliable primary periods. Primary-period and peak/trough detection excludes small local peaks and rejects ambiguous traces. After processing three measurements, switching power off correctly opens fitting and calculation instead of returning to parameter setup.
- Squared periods, fitting, area, heat-capacity ratio, and relative error now follow the already displayed and rounded values at every step. Decimal midpoint rounding is corrected and table/fit coordinates agree. Answers with valid precision but unequal values are rejected; no tolerance or hidden high-precision answer is used.
- Restores correct pointer picking when the screw interaction mirror is re-enabled after instructions. Removes the Real-helium candidate notice box without changing gas parameters or physical behavior.
- Separates file actions, experiment controllers, read-only views, learning, safe exit, and compatibility readers while preserving experiment, sampling, and persistence contracts. Closing the complete adiabatic materials window is independently undoable and restores tab order without rewinding the experiment.
- Hidden piston interaction mirrors stop rendering, and the standard simulation canvas avoids repeated size subscriptions and unchanged buffer resets. Physics steps and sampling are unchanged. Occasional long frames remain observable in the development preview.
- Single-figure P–T and P–N PDFs reserve space for their conclusions and keep section headings with their text, avoiding an extra conclusion-only page without changing report data.
- Update-manifest parsing uses patched js-yaml 4.3.2, retaining normal update metadata, localized release notes, and malformed-input limits with refreshed third-party records.
- The application ID, installer identity, user-data directory, and public update repository remain unchanged. Historical piston raw records and valid period readings are retained; fits and downstream calculations affected by obsolete rounding rules must be recomputed. Back up important experiments before upgrading.

## 6.4.0

- Adds per-experiment Piston-Oscillation Free-mode process review with an instrument-operation timeline, formal trace, selected-period evidence, and expandable score details.
- Reuses the established heat-capacity event colors, milestone nodes, and tooltip behavior while recording only actions that actually occurred, including repeated presses, resets, impacts, hose and power actions, and two-hand release gaps.
- Adds compact PDF report export for completed piston experiments, covering measurements, period processing, fitting, final calculation, process evidence, and scores without a separate theory chapter.
- Adds a Free-mode parameter sidebar for ambient pressure and temperature, sampling, the falling trigger, and input visualization, plus confirmed access to reviewed advanced model parameters.
- Freezes the complete parameter profile after the first formal curve is saved and continues to restore historical files from their captured model and parameter snapshots.
- Scales the allowed falling-trigger range with ambient pressure while retaining the reviewed 96–130 kPa window at standard conditions and respecting sensor limits.
- Keeps acquisition pause, save, live monitoring, and retry-after-missed-trigger behavior stable after process-review integration.
- Retains the application ID, installer identity, public update repository, and user-data directory for an in-place update from 6.3.1.

## 6.3.1

- Distinguishes a whole piston recording without a credible primary half-cycle from a usable trace with a narrow selection, reacquiring only the affected run while preserving evidence, settings, and completed runs.
- Changes Free-mode `t1 / t2 / T` and final `A / gamma / relative error` entry to editable batch validation without counting malformed drafts as formal errors; Guide Mode remains stepwise.
- Adds seeded late-trace time folds and peak/trough shoulder attenuation so late-period selection can naturally degrade fitting without changing the early waveform, 1000 Hz grid, or underlying thermomechanical trajectory.
- Uses one versioned `1.1 N·s/m` equivalent linear loss for new-experiment pressing and free oscillation while retaining captured `0.434 N·s/m` and other supported historical snapshots.
- Adds a short-lived side-contact loss for unequal hand-release timing without lifting the platform after one hand releases, changing gas stiffness, or introducing permanent friction.
- Presents acquisition with a 0.300 s delay and 0.55x pacing over the first 0.400 s of physical trace; this does not rescale samples, timestamps, periods, or calculations.
- Restores live monitoring and audio after a press that misses the falling trigger, allowing an immediate second press in Free and Guide modes.
- Keeps mode controls available on the primary processing view, locks them only inside the secondary calculation window, and fixes overflow of longer unified-validation actions.
- Retains the application identity, update source, user-data directory, saved traces, and historical model semantics for an in-place update from 6.3.0.

## 6.3.0

- Adds a continuous piston thermal, pressure-sensor, press, and virtual-hand acquisition chain while retaining the existing Free plan, period processing, fitting, and calculation workflow.
- Adds state-aligned power, hose, locking-screw, piston-vibration, and bottom-impact audio, with height-aware reset impacts and a silent threshold below 5 mm.
- Unifies Guide checklist, primary-control, and interaction-gate state so correct actions after reminders cannot be rejected by stale step conditions.
- Freezes Guide recording and visible time at 0.500 s before unlocking Pause, using the modeled equilibrium for each 80, 70, and 60 mm height and its distinct settling offset.
- Migrates previously saved internal baseline-wait states to current steps so hidden diagnostic steps cannot reappear or block resumed Guide sessions.
- Adds Enter confirmation to Guide acquisition parameters, matching Free Mode.
- Adds crisp clockwise and counterclockwise screw arrows to Guide and Demo, tolerates correct-direction motion beyond completion, and graduates reverse-direction feedback from a gentle correction to protected boundary blocking.
- Cuts Demo height adjustment, hose removal, and hose connection duration by 50% while preserving the existing motion cues.
- Retains the application ID, installer identity, update repository, and user-data directory for an in-place update from 6.2.1.

## 6.2.1

- Fixes the first Free acquisition render failure while the formal pressure curve is still incomplete, keeping trigger, live plotting, pause, save, and next-run progression continuous.
- Converts period-selection indices and counts to safe rendering types, including legacy bigint-shaped values, without changing selection gestures, endpoint rules, period verification, or precision.
- Restores the visible screw-release settling motion by redrawing the demand-driven 3D instrument whenever piston, screw, hose, or platform state changes.
- Removes all unsupported fixed rebound-velocity ranges. Normal peaks above 2 m/s remain intact while finite-value, physical-boundary, and numerical-divergence checks continue.
- Silently stops failed rebound or settling animations, recomputes the stable position from current physical conditions, retains experiment data, and prevents a stuck rebounding state.
- Normalizes non-resumable press, hold, free-fall, rebound, and short-animation state on restart while preserving Free plans, curves, drafts, selections, answers, fitting, calculations, and audit history.
- Adds local processing/calculation render recovery that preserves the workbench chrome and data, plus an outer recovery frame that retains the real minimize, maximize/restore, and close controls.
- Verifies 3–6-run and mixed system/custom-height workflows through selection, answer history, automatic calculation, fitting, results, instrument return, persistence, and explicit reset.
- Ships matching installer, blockmap, and update metadata after 261 test files, TypeScript checks, 468-license-record verification, and a production audit with zero known vulnerabilities.

## 6.2.0

- Completes piston-oscillation Free Mode with resumable 3–6-run plans, system and custom 10–80 mm targets, ordered progress, retry, deletion, whole-session reset, period verification, fitting, and automatic calculation handoff.
- Adds per-run 1–1000 Hz sampling and 96.0–130.0 kPa falling-threshold settings, dynamic monitoring ranges, immediate acquisition when the threshold is already met, and complete raw-sample, physical-snapshot, and answer-history records.
- Unifies experiment-count and Free-progress controls across both heat-capacity methods, including keyboard, outside-click, popover placement, reset, color, and destructive-action behavior.
- Makes left-side materials navigation mode-specific and restores the 3D instrument plus realtime-data layout after calculation closes.
- Repairs Demo, Guide, and Free transitions, Free exit semantics, screw visual travel and pointer sensitivity, processing return, and non-blocking startup recovery.
- Applies one loaded-gas equilibrium model across all three piston modes. Screw release produces a recordable one-way 0.2 s settling segment while nominal and exact heights remain distinct.
- Migrates existing piston files into the new Free-session and thermodynamic structures without fabricating missing historical evidence, and prevents the rigid 0 mm lower stop from producing a false savable run.
- Ships matching installer, blockmap, and update metadata after 259 test files, TypeScript checks, 468-license-record verification, and a production audit with zero known vulnerabilities.

## 6.1.1

- Adds the complete piston-oscillation heat-capacity-ratio experiment with Demo, Guide, normal 3D operation, three 80/70/60 mm acquisition runs, period processing, and calculation.
- Adds a pressable power control that gates parameter input, realtime plots, and recording; Guide starts with power-on and requires power-off after period selection, while Demo powers off automatically.
- Enforces strict Guide ordering: out-of-step controls animate to acknowledge input but cannot change physical state.
- Replaces the formal piston model with the audited hybrid refinement while preserving functional node, hierarchy, origin, motion-axis, hit-target, magnetic-snap, scale, and camera contracts.
- Updates Electron, js-yaml, PostCSS, installer tooling, generated legal notices, audio attribution, and 3D-model provenance; npm security audits report zero known vulnerabilities at release time.
- Passes a clean-Windows 5.3.1 → 6.1.1 same-path upgrade gate, including workspace migration and exact differential blockmap reconstruction.

## 5.3.1

- Completes multi-group adiabatic-expansion experiments with automatic progression, group-level calculation and scoring, process review, and report/figure/package exports.
- Adds separate, confirmed controls for restarting only the current experiment or the current group without discarding other completed groups.
- Improves report hierarchy, three-line tables, scientific figure styling, and Chinese/Latin font consistency.

## 5.2.0

- Moves V3 workspace projection, fingerprinting, generation commits, and read-back verification into a background Worker, while semantic saves use bounded debounce and continuous runs checkpoint at most once every 15 seconds.
- Preserves valid standard, ideal-gas, and heat-capacity workspaces written by 4.2.3 and 5.1.1. Data written by the withdrawn 5.1.2 build is outside the compatibility guarantee.
- Bounds Free traces to 800 samples and 320 detailed events per branch, 4 detailed branches per trial, and 7 completed trials plus the active trial per parameter domain.
- Retries temporary persistence failures, prunes invalid candidates after quota failures, retains the last verified generation, and keeps save errors non-blocking.

## 5.1.2 (withdrawn)

- This experimental build is withdrawn. Its workspace data is outside the compatibility guarantee for later stable versions.

## 4.1.7

- Publishes the first acceptance release from the public release repository.
- Adds Help → User Guide in the desktop app, opening the language-appropriate public README.

## 4.1.6

- Migrates desktop auto updates to the public release repository while keeping the existing installer and user-data identities.
