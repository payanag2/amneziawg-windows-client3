# MyAmneziaWG3 for Windows

MyAmneziaWG3 is an independent Windows desktop client based on the tested MyAmneziaWG fork. It is designed to install alongside the official AmneziaWG client and the separate MyAmneziaWG client.

## Separate application identity

MyAmneziaWG3 uses its own:
- Product name, installer UpgradeCodes, and MSI component GUIDs
- Installation and configuration directory: `Program Files\MyAmneziaWG3\Data`
- Windows manager and tunnel service names
- Registry namespace: `Software\MyAmneziaWG3`
- UI window class and application branding

The installer does not remove the shared Wintun driver during uninstall, avoiding disruption to other VPN clients that may use it.

## Build

The GitHub Actions workflow **Build MyAmneziaWG3** builds the Windows binaries and MSI installers for x86, amd64, and arm64. The generated installers are available as workflow artifacts.

To publish a GitHub Release, open **Actions → Release MyAmneziaWG3 → Run workflow** and enter a tag such as `v1.0.0`. If the tag does not exist, the workflow creates it from the current `main` branch, builds the installers, and attaches them to the release.

## Documentation

- [Build and development notes](docs/buildrun.md)
- [Admin registry settings](docs/adminregistry.md)
- [User registry settings](docs/userregistry.md)
- [Security design](docs/attacksurface.md)
- [Enterprise notes](docs/enterprise.md)
- [Network behavior](docs/netquirk.md)

## License

This repository retains the upstream MIT licensing terms. See [COPYING](COPYING).
