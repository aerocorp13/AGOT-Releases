# AGOT Desktop — African Geospatial Operational Twin

Official Windows installer distribution for [GeoTwins Africa](https://geotwins.org/download/).

AGOT is a desktop geospatial workstation under development for local GIS, terrain-aware 3D scenes and spatial planning workflows. Supported capabilities and limits are described for each tested release.

## Downloads

The initial Windows x64 **v1.0.0 public preview** was published on 29 October 2026. The public GitHub release is uploaded, but that alone does **not** establish complete clean-Windows installation, code-signing, or licensing acceptance. Download published installers from [Releases](https://github.com/aerocorp13/AGOT-Releases/releases) or the official [GeoTwins download page](https://geotwins.org/download/). Draft releases are not public downloads.

The first published preview asset is `AGOT.Desktop_1.0.0_x64_en-US.msi`. Future releases may use `AGOT-Setup-x64.msi` or a versioned Windows MSI/EXE name. Do not assume that every release includes a separate checksum, EULA or notice until those assets are actually present. Check each release's real files and notes. The GeoTwins website **automatically discovers the newest eligible published Windows installer** via GitHub's public Releases API when visitors open `/download/`; new releases do not require a website redeployment. This is **not** automatic updating of already installed copies.

Verify a downloaded installer in PowerShell:

```powershell
Get-FileHash -LiteralPath ".\AGOT.Desktop_1.0.0_x64_en-US.msi" -Algorithm SHA256
```

Compare the complete hash with that release's checksum file. Inspect Properties → Digital Signatures, or use `Get-AuthenticodeSignature`, to check signing. An unsigned preview will be explicitly identified and may display Windows SmartScreen warnings. Do not assume an installer is signed.

## Source and licensing

This repository contains public distribution documentation and release metadata only. AGOT's application source remains private and is not supplied in GitHub's automatically generated source archives for this repository.

The repository's MIT license covers its public documentation and metadata; it does not license the separately distributed AGOT application or grant access to private source. Any installer must include its approved end-user terms and third-party notices. Required third-party source delivery is provided separately where applicable.

## Support

Website: [geotwins.org](https://geotwins.org) · Support: [admin@geotwins.org](mailto:admin@geotwins.org)

Report security concerns using [SECURITY.md](SECURITY.md). Automatic application updates are not enabled for the initial installer release.
