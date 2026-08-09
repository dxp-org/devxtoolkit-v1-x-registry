# devxtoolkit-v1-x-registry

Install/distribution index for [devxtoolkit-v1](https://github.com/dxp-org/devxtoolkit-v1-x). Schema mirrors the format already used by `marlin-registry` and `marlin/packages/marlin/registry` (`apiVersion: marlin/v1`, `kind: Registry`/`Package`), so this can be resolved by Marlin's package manager once it's built (currently not yet built — Wave 5, `INIT.19.xx`), or read directly by anyone in the meantime.

## Layout

```text
index.yaml                       # Registry entry point — lists packages
manifests/devxtoolkit-v1.yaml    # Package manifest — install/uninstall steps
```

## Why this exists as a separate repo

devxtoolkit-v1 is source-distributed (PowerShell scripts, not a compiled
binary), so there's no fixed release-artifact/checksum pattern the way
`niji`'s `github-release` zip manifest has. This registry entry installs
by cloning `devxtoolkit-v1-x` and running its existing installer script
(`src/core/DevXToolkit-Installer-v1.0.ps1`), rather than inventing new
install logic.

## Status

Manifest points at the pinned `v1.3.0` source tag for reproducible installs on
Windows, Linux, and macOS. DevXToolkit `1.3.0` is also published to PSGallery.

## License

MIT — see [`LICENSE`](LICENSE).
