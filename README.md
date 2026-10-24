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

Build and automated validation passed.
## Attribution and licensing

Built on Charles Vestal's [fm1-amb](https://github.com/charlesvestal/fm1-amb) and fm1-base, with third-party components including Mutable Instruments Rings/stmlib. See [licensing notes](LICENSING.md) and the individual source/vendor notices in the complete source archive.

### Sequencers

- **Original** — the original AMB-1 generative sequencing by [Charles Vestal](https://github.com/charlesvestal/fm1-amb), retained and extended for genAMB (MPL-2.0).
- **Hallucigenia (formerly Evolve)** — genAMB's independent generative sequencer implementation, inspired by the [Extratone Darwinism](https://library.vcvrack.com/Extratone/Darwinism) concept. It is not a direct port of Darwinism; the implementation in `app/dsp/evolve.c` is MPL-2.0.
- **Proteus** — adapted from [Seaside Modular Proteus](https://github.com/abluenautilus/SeasideModularVCV/blob/master/src/Proteus.cpp), by Seaside Modular contributors (MIT). The FM-1 adaptation uses fixed-size state and follows the active chord.
- **UNIT-D / UnitDistanceSeq** — adapted from [Animatek's UNIT-D](https://github.com/animatek/UZZ-VCV-RACK/blob/main/src/UnitDistanceSeq.cpp). The genAMB adaptation is GPL-3.0-or-later, with upstream attribution and license text retained in `app/vendor/unitd/`.

These are hardware-specific implementations/adaptations. Original component copyright and license notices remain in the complete source archive; see [LICENSING.md](LICENSING.md) for the combined firmware's licensing details.
