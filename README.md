# genAMB FM-1

Custom FM-1 firmware. Current version: **1.0 RC1**.

## Downloads

- [Precompiled firmware](firmware/genAMB-1.0-RC1.fwsc?raw=true)
- [Complete source archive](source/genAMB-1.0-RC1-Complete-Source.zip?raw=true)
- [Release notes and validation summary](docs/Release-Notes-1.0-RC1.md)
- [Build instructions](docs/BUILDING-1.0-RC1.md)
- [Checksums](SHA256SUMS)

The source ZIP includes application code, fm1-base, vendored DSP code, tests, and their license notices. Extract it before building. The compiler, SDK resources, and fonts are external to this source archive; see the build instructions.

## RC1

Includes the Garden and Root & Note Div pages, 2×2 Setup controls, larger panel text with two-line values, and genAMB USB branding. Displayed version: `1.0 RC1`. Updater identity: `FM-1_7179912` (internal release `17.99.12`).

Build and automated validation passed. Physical FM-1 boot/audio testing remains required. The previously reported high-octave FM loudness issue remains unresolved. No audio DSP changes were made for RC1.

## Attribution and licensing

Built on Charles Vestal's [fm1-amb](https://github.com/charlesvestal/fm1-amb) and fm1-base, with third-party components including Mutable Instruments Rings/stmlib. See [licensing notes](LICENSING.md) and the individual source/vendor notices in the complete source archive.
