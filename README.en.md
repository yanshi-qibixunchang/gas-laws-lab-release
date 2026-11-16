# Gas Laws Lab

[简体中文](./README.md) · [繁體中文](./README.zh-TW.md)

Gas Laws Lab is a Windows experiment workbench connecting 3D apparatus interaction, physical simulation, data acquisition, guided calculation and local reports. It covers hard-sphere molecular dynamics, ideal-gas relations, and air/helium heat-capacity-ratio experiments.

**Current stable version: 6.5.3**

[Download for Windows x64](https://github.com/yanshi-qibixunchang/gas-laws-lab-release/releases/download/v6.5.3/heat-capacity-lab-setup-6.5.3.exe) · [Release notes and assets](https://github.com/yanshi-qibixunchang/gas-laws-lab-release/releases/tag/v6.5.3) · [Release verification](docs/releases/v6.5.3.md) · [Source Release](https://github.com/yanshi-qibixunchang/gas-laws-lab-history/releases/tag/v6.5.3)

## Experiments

| Experiment | Workflow |
| --- | --- |
| Standard hard-sphere simulation | 3D molecular motion, live charts, statistics and results |
| Ideal-gas relations | P–T, P–V and P–N sampling, fitting, verification and history |
| Adiabatic expansion | Apparatus operation, pressure and temperature signals, repeated trials, heat-capacity ratio and uncertainty |
| Piston oscillation | Press/release and period measurement; unknown-volume multi-height fitting, or known-total-volume direct calculation for one realistic-air trial |

Both heat-capacity methods support **air/helium**, **ideal/realistic conditions**, and Demo, Guide and Free modes. The interface supports Simplified Chinese, Traditional Chinese and English, with light and dark themes. The desktop app exports supported PDF reports, PDF/PNG figures, CSV files and data packages.

## What changed in 6.5.3

- Realistic air and helium now include dynamic-pressure internal dissipation and matching gas heating alongside external heat transfer. Residual mechanical loss, thermal response, sensor response and tail disturbance presets are updated with nonzero active coefficients.
- New experiments, full resets and restored defaults use the new profiles. Historical experiments retain their model versions, parameter snapshots and records. Known-volume and multi-height calculations remain compatible; third-party dependency versions are unchanged.
- The fixed air comparison reaches waveform R² = 0.9589 over the first 100 ms, but peak and envelope errors remain above their limits; 4 of 16 held-out curves pass all four gates. Air passes the five operating conditions. The original helium batch has three failing rolling three-trial means and no measured waveform validation. These are accepted teaching presets, not a claim of complete apparatus calibration.

## Install and upgrade

Download the installer and follow its setup wizard. Users on **6.5.2 or earlier** can check for updates in the app or save and close the app before installing the full package into the existing location.

The application identity and user-data location remain unchanged. Historical experiments retain their model and parameter snapshots, raw records and calculation progress; new experiments use current profiles. Existing migration rules still apply to older formats.

Core experiments run locally without an account. The browser and desktop editions save progress separately; installing the app does not transfer browser experiments. The browser supports the simulation and calculation UI, while report, figure and table export requires the Windows desktop app.

## Model scope

Ideal/realistic refers to experimental conditions. Ideal conditions still require correct operation. Realistic profiles include thermal, mechanical and measurement effects with explicitly limited validation; they do not reproduce every physical apparatus. Some helium acceptance ranges are scaled from the agreed air ranges using the theoretical ratio; they are not helium measurements.

The 3D apparatus is an interaction and visualization layer; the software's physical model produces numerical results. The adiabatic apparatus draws on several teaching instruments, including FD-NCD-C, and is not an official simulation or digital replica of that product. Model, audio and physics references are available in the app's About pages and [third-party notices](https://github.com/yanshi-qibixunchang/gas-laws-lab-history/blob/v6.5.3/THIRD_PARTY_NOTICES.md).

## Downloads and update assets

Use Help → About to check for updates. This repository provides the matching installer, `.exe.blockmap` and `latest.yml`. If a network issue prevents automatic updating, install the full package over the existing location.

This repository contains release material only. Development source, build instructions and version tags are available in the [public source history](https://github.com/yanshi-qibixunchang/gas-laws-lab-history/tree/v6.5.3). See [CHANGELOG.md](CHANGELOG.md) for past versions. Data from the withdrawn 5.1.2 experimental build is outside the compatibility guarantee.

## Rights and feedback

No open-source license is declared for the project source. Public access does not grant redistribution rights. Dependencies, fonts, audio, models and exporter components retain their recorded terms or rights status, with an exact-version third-party inventory in the app. See [THIRD_PARTY_NOTICES.md](https://github.com/yanshi-qibixunchang/gas-laws-lab-history/blob/v6.5.3/THIRD_PARTY_NOTICES.md), [SECURITY.md](SECURITY.md) and [CONTRIBUTING.md](https://github.com/yanshi-qibixunchang/gas-laws-lab-history/blob/v6.5.3/CONTRIBUTING.md).

For feedback, include the app version, experiment, gas and conditions, reproduction steps and screenshots. Remove personal information before sharing experiment files. Post-release fixes will be documented in subsequent patch versions.
