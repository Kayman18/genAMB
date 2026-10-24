# genAMB FM-1 — 1.0 RC1

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
