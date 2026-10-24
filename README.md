# genAMB FM-1 — 1.0 RC2

Custom firmware for the FM-1. RC2 replaces the earlier independent Hallucigenia/Evolve implementation with a port of the upstream Hallucigenia sequencing core for **both Rings and FM**.

## Downloads

- [Precompiled RC2 firmware](firmware/genAMB-1.0-RC2-Hallucigenia-Port.fwsc?raw=true)
- [Complete RC2 source archive](source/genAMB-1.0-RC2-Complete-Source.zip?raw=true)
- [Release notes and validation summary](docs/Release-Notes-1.0-RC2.md)
- [Build instructions](docs/BUILDING-1.0-RC2.md)
- [SHA-256 checksums](SHA256SUMS)

Extract the source ZIP before building. It includes the application, platform code, vendored DSP sources, original upstream Hallucigenia source, tests, and license notices. The compiler, SDK resources and fonts are external to this archive; see the build instructions.

## Hallucigenia in RC2

The port preserves upstream randomization, all-16-step mutation, advance-before-output clock behavior and sample-and-hold ordering. Original, Proteus and UNIT-D remain selectable.

FM-1 adaptations retain the system clock, all 13 rate settings, scale/chord following, octave controls, humanization, Burst and existing pattern storage. End-of-pattern triggers mutation automatically. Existing RC1 pattern banks remain loadable; saved pitches retain their 7-bit encoding.

**After reset, the first clock plays the second visible step**, matching upstream. This is a sequencing-core port, with the existing FM-1 interface. See [upstream and adaptation details](docs/Hallucigenia-Upstream.md).

Display version: `1.0 RC2`. USB manufacturer/product: `genAMB` / `genAMB FM-1`. Numeric updater identity: `FM-1_7179913` (internal release `17.99.13`).

The build passed 10,000 comparisons against the upstream module core, production integration and regression tests, and package integrity checks. See the release notes for test scope, resource use and remaining limitations.

## Attribution and licensing

Built on Charles Vestal's [fm1-amb](https://github.com/charlesvestal/fm1-amb) and [fm1-base](https://github.com/charlesvestal/fm1-base), with [felucca-bsp](https://github.com/hugelton/felucca-bsp) by Leo Kuroshita / Hügelton Instruments. Synthesis components include Mutable Instruments Rings/stmlib by Emilie Gillet and the [Zen-1](https://github.com/aceyprime/zen-1) six-operator FM engine and its msfa-derived core.

### Sequencers

- **Original** — original AMB-1 generative sequencing by [Charles Vestal](https://github.com/charlesvestal/fm1-amb), retained and extended for genAMB (MPL-2.0 provenance).
- **Hallucigenia / Darwinism** — ported from [Eater of Sheep's Extratone / XTRTN source](https://github.com/EaterOfSheep/Extratone/blob/main/src/Darwinism.cpp), GPL-3.0-or-later. RC2 replaces the independent Evolve implementation with this upstream-derived core.
- **Proteus** — adapted from [Seaside Modular Proteus](https://github.com/abluenautilus/SeasideModularVCV/blob/master/src/Proteus.cpp), by Seaside Modular contributors (MIT).
- **UNIT-D / UnitDistanceSeq** — adapted from [Animatek's UNIT-D](https://github.com/animatek/UZZ-VCV-RACK/blob/main/src/UnitDistanceSeq.cpp); the adaptation is GPL-3.0-or-later.

Original copyright and component license notices are retained in the complete source archive. See [LICENSING.md](LICENSING.md) for component provenance and combined-firmware licensing.
