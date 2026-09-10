# Sonic 3 PTR - Prototype Revisited

A web port of Sonic 3 A.I.R. (Angel Island Revisited) modified to run the **Sonic 3 November 1993 prototype ROM** instead of the final Sonic 3 & Knuckles ROM.

This project compiles the Sonic 3 A.I.R. source code with Emscripten/WebAssembly, patches the ROM validation to accept the prototype ROM (2MB, Murmur2 checksum `0x6e8e95a6b2e4648f`), and serves it as a browser-playable web app.

### How to play

1. Open the hosted web build
2. Wait for the engine data to load
3. Upload the **Sonic 3 (1993-11-03)** prototype ROM (`.md` or `.bin`)
4. Play!

### Building

The GitHub Actions workflow (`build-web.yml`) handles the full build:
- Checks out the source with submodules
- Builds with Emscripten + Ninja
- Packages engine data, game data, scripts, config, and oxygenproject into `sonic3air.data`
- Produces a web artifact with `.wasm`, `.js`, `.html`, and `.data`

### Credits

Based on [Sonic 3 A.I.R.](https://sonic3air.org/) by Eukaryot (GPLv3).
Prototype ROM analysis and disassembly by Esrael Neto (Sonic Delta).

### Disclaimer

Sonic 3 A.I.R. is a non-profit fan game project, not affiliated with SEGA or Sonic Team.
