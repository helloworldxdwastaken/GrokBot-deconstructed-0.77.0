# GrokBot deconstructed 0.77.0

> **Unofficial university study project.** Not affiliated with or endorsed by
> Anysphere (Cursor), xAI or SpaceX. This repository contains **no** Grok Bot
> code, binaries or decompiled output, only our own tooling and write-ups.
> Read [LEGAL.md](LEGAL.md) before using it.

A reproducible pipeline for studying how the Grok Bot macOS desktop app is
built. It takes the copy installed on your own Mac and produces, **locally**:

- the unpacked Electron archive (`app.asar`);
- Prettier-formatted versions of every JS/CSS/HTML bundle;
- arm64 slices of each first-party native binary; and
- a Ghidra project plus decompiled C, imports, exports and strings per binary.

The repository adds write-ups of what we found and what changed between
versions:

- [docs/FINDINGS-0.75.8.md](docs/FINDINGS-0.75.8.md): architecture, runtimes
  and native components of 0.75.8;
- [docs/CHANGES-0.75.8-to-0.77.0.md](docs/CHANGES-0.75.8-to-0.77.0.md): new
  features, removals and native changes in 0.77.0, and how they were found.

## Requirements

- macOS on Apple Silicon with Grok Bot installed in `/Applications`
- Node.js (for `npx`), Xcode Command Line Tools (`lipo`, `otool`)
- JDK 21: `brew install openjdk@21`
- [Ghidra](https://github.com/NationalSecurityAgency/ghidra/releases) 12.x,
  unzipped anywhere

## Usage

```sh
GHIDRA=/path/to/ghidra_12.1.4_PUBLIC scripts/recover-installed-app.sh
```

The script reads the version from the app's `Info.plist` and rebuilds
`recovered/<version>/` from scratch. That takes about 45 minutes, most of it
Ghidra on the Swift and Rust binaries. `recovered/` is gitignored. **Do not
commit or share it** (see [LEGAL.md](LEGAL.md)).

To compare two versions, run the script once per installed version. Earlier
`recovered/<version>/` folders are kept. The comparison method is described in
[docs/CHANGES-0.75.8-to-0.77.0.md](docs/CHANGES-0.75.8-to-0.77.0.md#method).

## License

The scripts and documentation in this repository are released under the
[MIT License](LICENSE). That licence covers **only our own work**. It grants no
rights in Grok Bot or in anything the script extracts from it.
