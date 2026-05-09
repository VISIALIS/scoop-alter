# Scoop bucket for Alter

[Scoop](https://scoop.sh) bucket distributing Alter on Windows. Three packages :

| Package | Description |
|---------|-------------|
| `alter-cli` | CLI to classify EVM addresses |
| `alter-mcp` | MCP server (Model Context Protocol) exposing Alter to AI agents |
| `alter` | Desktop GUI (Flutter) |

The binaries are mirrored from the `VISIALIS/homebrew-alter` public Releases (built and uploaded by the CI of the private `VISIALIS/phoenix_0` repository).

## Install

```powershell
scoop bucket add visialis https://github.com/VISIALIS/scoop-alter
scoop install visialis/alter-cli
scoop install visialis/alter-mcp
scoop install visialis/alter
```

After install :

```powershell
alter-cli --version
alter-mcp --version
# Desktop : "Alter" available in the Start Menu (shortcut)
```

## Update

```powershell
scoop update
scoop update alter-cli alter-mcp alter
```

## Uninstall

```powershell
scoop uninstall alter-cli
scoop uninstall alter-mcp
scoop uninstall alter
scoop bucket rm visialis
```

## Verification

The binaries are signed by GitHub Actions. SHA-256 hashes are pinned in each manifest and checked by Scoop on download.

Source workflow : [`.github/workflows/cd.yaml`](https://github.com/VISIALIS/phoenix_0/blob/main/.github/workflows/cd.yaml) (private repo, accessible to VISIALIS members).

## Maintenance

The manifests are auto-updated by [Excavator](https://github.com/lukesampson/scoop/wiki/App-Manifest-Autoupdate) once a new release lands on `VISIALIS/homebrew-alter`. The workflow is in `.github/workflows/excavator.yml`.

Manual update :

```powershell
scoop install excavator
excavator
```

## Other distribution channels

- macOS / Linux : `brew install VISIALIS/alter/alter-cli` (cf [homebrew-alter](https://github.com/VISIALIS/homebrew-alter))
- Mobile : App Store / Google Play (cf [alter.visialis.fr](https://alter.visialis.fr))
- Web : [alter.visialis.fr](https://alter.visialis.fr)

## License

Proprietary — see [VISIALIS](https://github.com/VISIALIS).
