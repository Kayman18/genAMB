# genAMB FM-1 — 1.0 RC1

Built from v17.99.11 with all approved pending UI and branding changes.

## Changes

- Garden page 1: 2×2 Tempo, Evolve, Motion and Drift controls.
- Garden page 2, Root & Note Div: Root, FM Density, Rings Density and an empty fourth box. Press HOME to switch between Garden pages. The controls edit the existing parameters; the original FM/Rings density controls are removed. Sequencer-specific algorithm density parameters remain separate.
- GLO Setup: 2×2 Tune, MIDI out, Lights and an empty fourth box.
- Shared panel typography enlarged with measured fitting. Two-word values such as Smooth Rnd use two lines where they fit; captions and knob indicators retain separate space. Active panel borders remain, with bottom underlines removed where they could touch two-line values.
- USB manufacturer: genAMB. USB product: genAMB FM-1.
- Displayed version: 1.0 RC1. Numeric updater identity: FM-1_7179912 (internal release 17.99.12).

All v17.99.11 layouts and fractional Rate settings are retained. No audio DSP, parameter IDs or saved-project format changed. Project format remains 22. FM maximum remains six voices, default four. FM filter remains on CPU1. The previously reported high-octave FM loudness issue is unresolved; this UI/branding release does not change its sound.

## Validation

- Production host tests passed for 18 wide pages, all physical knob bindings in both prior row states, new Root/Note controls, exclusive placement of FM/Rings density controls, and M1–M6 fixed routing/shape with adjustable depth/speed.
- HOME navigation Garden ↔ Root & Note Div, GLO Setup, Rings/Delay 2/UNIT-D, PAD and Reverb navigation passed. Native screenshots inspected, including two-line Shape values.
- Existing pending layout/rate tests and project/filter migration tests passed.
- Sanitized FM sequencer, 102 worker-policy checks, FM port (84 checks), UNIT-D and classic filter regression tests passed.
- JieLi PI32v2 hardware build passed memory, RAM-resident code, arithmetic and register-access checks. Only existing upstream Rings unused-typedef warnings remain.
- Package CRCs, loader, decrypted application bytes and padding verified. New USB names and display version confirmed in the application binary.
- No physical FM-1 boot or listening test was possible here. After flashing, check USB naming, both HOME pages, stored project recall, and audio playback.

## Size and memory

Firmware: 610108 bytes. Application: 309992 bytes.
Normal RAM: 96256 / 98304 bytes (2048 free).
Pool: 269684 / 344064 bytes (74380 free).

SHA256: `0f95beb86b1a6b304658182edbda31ae35fb60c24019d3e3d04bd844255bff14`

The source archive includes the matching code and build instructions. Compiler, SDK resources and fonts remain external as in previous releases.
