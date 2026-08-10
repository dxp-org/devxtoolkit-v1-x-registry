# devxtoolkit-v1-x-registry

Install/distribution index for DevXToolkit v1. Schema mirrors the format already used by `marlin-registry` and `marlin/packages/marlin/registry` (`apiVersion: marlin/v1`, `kind: Registry`/`Package`), so this can be resolved by Marlin's package manager once it's built (currently not yet built — Wave 5, `INIT.19.xx`), or read directly by anyone in the meantime.

## Layout

```text
index.yaml                       # Registry entry point — lists packages
manifests/devxtoolkit-v1.yaml    # Package manifest — install/uninstall steps
```

## Why this exists as a separate repo

DevXToolkit v1 is distributed publicly through PowerShell Gallery. The
implementation source repository remains private; this public registry is the
stable distribution/support surface for installers and portfolio tooling.

## Status

Manifest points at PowerShell Gallery version `1.6.0` for reproducible installs
on Windows, Linux, and macOS.

## License

MIT — see [`LICENSE`](LICENSE).
