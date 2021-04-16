# termite-flatpak

A [Flatpak](https://flatpak.org/) manifest for the [termite](https://github.com/thestinger/termite) terminal emulator

## Important note

Unfortunately, there is little to no practical value to run terminal emulators with Flatpak due to the [sandbox](https://docs.flatpak.org/en/latest/basic-concepts.html#sandboxes). There is [no way to disable the sandbox](https://github.com/flatpak/flatpak/issues/1699) (either for a specific app or globally). It is possible to “poke holes in it” but [it requires modifications of the source code](https://github.com/flatpak/flatpak/issues/1699#issuecomment-411233968) and is simply not worth it.

Due to the aforementioned restriction, the manifest is far from complete and only provides minimal instructions for the build. There is no cleanup, exports, etc.

## Build

```shell
flatpak-builder build --install --force-clean --user dev.micay.daniel.Termite.yml
```

## Run
```shell
flatpak --user run dev.micay.daniel.Termite
```
