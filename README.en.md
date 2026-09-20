# Gas Laws Lab

[简体中文](./README.md) · [繁體中文](./README.zh-TW.md)

## Introduction

Gas Laws Lab is a Windows desktop application for thermal and molecular-motion experiments. It includes standard hard-sphere simulation, ideal-gas relation studies, and air heat-capacity-ratio experiments using both adiabatic expansion and piston oscillation.

This public release repository contains Windows installers, auto-update assets, and multilingual release notes. Reviewed, anonymized source history is published separately in [gas-laws-lab-history](https://github.com/yanshi-qibixunchang/gas-laws-lab-history); private research-report working material is outside that mirror.

## Download and installation

The latest stable release is [`v6.4.2`](https://github.com/yanshi-qibixunchang/gas-laws-lab-release/releases/tag/v6.4.2). Download `heat-capacity-lab-setup-6.4.2.exe` from Releases, verify that it came from this repository, and run it.

The application ID, installer identity, user-data directory, and public update repository remain unchanged. Historical piston raw records and valid period readings are retained; fits and downstream calculations affected by obsolete rounding rules must be recomputed. Back up important experiments before upgrading.

Data written by the withdrawn experimental 5.1.2 build remains outside the compatibility guarantee. Back up the user-data directory before following any recovery instructions.

## Auto update

Open **Help → About** and click **Check for Updates**. A stable update requires all three matching files in the same GitHub Release:

- `heat-capacity-lab-setup-6.4.2.exe`
- `heat-capacity-lab-setup-6.4.2.exe.blockmap`
- `latest.yml`

If automatic update fails, download the latest installer and install it over the existing copy. An uninstall is not required unless a Release explicitly documents an incompatibility.

## Patch changes in 6.4.2

Version 6.4.2 restores supported older piston workspaces after upgrade, preserves raw experiment records, and invalidates obsolete fits and calculations under the current refitting rules. It also repairs clean dependency installation, strengthens Windows upgrade verification, and reviews development records. Experiment operation and exact checks based on displayed values are unchanged.

- **Restore older piston experiment files**: Adds strict version migrations for older piston Free sessions and measurements so records still present in storage can appear again. Raw samples, frozen parameters, and valid period readings are retained in the experiment group; obsolete fits and downstream calculations require recomputation. Unknown fields, future versions, and damaged evidence remain preserved and quarantined, with no relaxation of exact answer checks.
- **Repair clean dependency installation**: Adds the missing @emnapi/runtime 1.11.3 peer required by an optional WASM build branch, resolving rejection by newer npm versions. A regression check covers all required peers; existing dependency versions, URLs, and integrity values are preserved.
- **Check dependencies before upgrade testing**: The Windows upgrade workflow installs locked dependencies before downloading or installing either app. Legacy probes are restricted to clean hosted Windows runners, verify the original file identity, and restart again after upgrade to confirm persistence. Ordinary local execution is rejected before launching an old app.
- **Review development records and indexes**: Reviews links, version context, and identity information in new current documents; adds the missing architecture-composition index; and distinguishes historical candidates, releases, and incomplete checks. Archived plans and model scans are not reclassified as pending work or physical calibration.
- **6.4.2 patch update and compatibility**: Retains the application ID, installer identity, user-data directory, and update repository, with the installer and complete update assets. Experiment behavior, state ownership, persistence, and exact answer checks match 6.4.1. Obsolete fits and downstream calculations from earlier piston versions still require recomputation.

## Highlights in 6.4.1

Version 6.4.1 completes Real/Ideal conditions, air/helium profiles, and staged learning for both heat-capacity experiments. It fixes piston primary-cycle detection, power-off handoff, and exact calculations from displayed values, with workbench, persistence, performance, and report improvements.

- **Real/Ideal and air/helium profiles for both methods**：Both methods support Real/Ideal experiment conditions and air/helium. Ideal presets remove modeled environmental, observation, and loss disturbances while retaining manual operation, processing, and calculation. Incorrect operation still has physical consequences; Ideal provides diagnostics without numerical scores.
- **Staged learning with Free-mode retention**：First use records familiarity with each method and unlocks Demo, Guide, and Free in sequence where learning is needed. Demo and unfinished Guide sessions do not become Free experiments. Completed guides remain reviewable, and Free data survives mode switching until a full reset.
- **At least two primary periods and a correct power-off handoff**：Guided selections require at least two reliable primary periods. Primary-period and peak/trough detection excludes small local peaks and rejects ambiguous traces. After processing three measurements, switching power off correctly opens fitting and calculation instead of returning to parameter setup.
- **Exact answers calculated step by step from displayed values**：Squared periods, fitting, area, heat-capacity ratio, and relative error now follow the already displayed and rounded values at every step. Decimal midpoint rounding is corrected and table/fit coordinates agree. Answers with valid precision but unequal values are rejected; no tolerance or hidden high-precision answer is used.
- **Clear workbench responsibilities and undo boundaries**：Separates file actions, experiment controllers, read-only views, learning, safe exit, and compatibility readers while preserving experiment, sampling, and persistence contracts. Closing the complete adiabatic materials window is independently undoable and restores tab order without rewinding the experiment.
- **Patch the update-manifest parser dependency**：Update-manifest parsing uses patched js-yaml 4.3.2, retaining normal update metadata, localized release notes, and malformed-input limits with refreshed third-party records.
- **Retain raw records and recompute obsolete calculations**：The application ID, installer identity, user-data directory, and public update repository remain unchanged. Historical piston raw records and valid period readings are retained; fits and downstream calculations affected by obsolete rounding rules must be recomputed. Back up important experiments before upgrading.

Occasional long frames remain possible in the development preview. Read this Release for compatibility details.

## Experiment modules

### Heat-capacity ratio by adiabatic expansion

Demo, Guide, and Free modes cover zeroing, pumping, waiting, rapid release, recovery, U₀/U₁/U₂ records, multi-group experiments, calculation, scoring, process review, and report export.

### Heat-capacity ratio by piston oscillation

Version 6.4.0 completes the course-result loop on top of the continuous thermal, sensor, and virtual-hand acquisition model stabilized in 6.3.1:

- Free Mode adds per-experiment process review and scoring. Switching the experiment number updates its instrument timeline, formal trace, selected period, evidence, and expandable score details together.
- Ordinary actions and major saved-curve milestones reuse the established heat-capacity colors, nodes, and tooltip treatment. Re-presses, resets, bottom impacts, hose and power actions, and two-hand release gaps appear only when they actually occurred.
- Completed Free experiments can export a compact PDF report covering the file, recorded measurements, periods, fit, final calculation, process evidence, and scores without a separate theory or formula chapter.
- The Free-mode parameter sidebar exposes ambient pressure and temperature, sampling, the falling trigger, and input visualization. Reviewed advanced parameters require explicit confirmation, and the complete profile freezes with the experiment file after its first formal trace is saved.
- The allowed falling-trigger range scales with ambient pressure while retaining the reviewed `96–130 kPa` window at standard conditions and staying inside sensor limits.
- Acquisition remains pausable, saveable, and retryable after process-review integration, including monitoring after a press that misses the trigger.

### Standard and ideal-gas simulations

Standard Simulation provides hard-sphere molecular motion, realtime sampling, and result charts. Ideal Gas supports `P-T`, `P-V`, and `P-N` scans, fitting, and verification.

## Release notes and validation

- `CHANGELOG.md`: user-facing version history.
- `docs/releases/release-notes.json`: structured trilingual notes used by the in-app update window.
- GitHub Releases: installers, update metadata, and complete notes for each version.

Version 6.4.2 passed strict TypeScript checks, all 349 automated test files, production and full dependency audits with zero vulnerabilities, clean dependency installation, a complete Windows build, and all three update-asset checks. Exact 6.4.1 → 6.4.2 differential reconstruction copied 74.9% of bytes. Four-file browser regression, mode changes, parameters, window history, and restoration passed; the packaged app retained a changed parameter after clean exit and relaunch.

Clean Windows 6.4.0 → 6.4.2 follow-up validation and 6.4.1 → 6.4.2 in-place upgrades both passed, including old-version relaunch, workspace and database restoration, differential reconstruction, and clean exit.

## FAQ

**Will upgrading remove old experiments?**  
The application ID, installer identity, user-data directory, and public update repository remain unchanged. Historical piston raw records and valid period readings are retained; fits and downstream calculations affected by obsolete rounding rules must be recomputed. Back up important experiments before upgrading.

**Why does Realtime Data show only “Power off”?**  
This is the normal off state in the piston-oscillation experiment. Press the power control on the 3D instrument first.

**What if auto update fails?**  
Download the 6.4.2 installer from Releases and install it over the existing copy while retaining the user-data directory.

**Why might Windows show a safety warning?**  
Windows may warn about internet-downloaded installers that have not accumulated enough reputation. Verify the repository URL and Release file name before continuing.
