# AGOT Desktop — African Geospatial Operational Twin

Official Windows installer distribution for [GeoTwins Africa](https://geotwins.org/download/).

AGOT is a desktop geospatial workstation under development for local GIS, terrain-aware 3D scenes and spatial planning workflows. Supported capabilities and limits are described for each tested release.

## Downloads

**No Windows installer is approved or published yet.** Get approved installers only from this repository's [Releases](https://github.com/aerocorp13/AGOT-Releases/releases) page or the official [download page](https://geotwins.org/download/). A draft release is not a public download.

Published MSI assets use the name `AGOT-Setup-x64.msi`. Each release includes `SHA256SUMS.txt`, installation requirements, known limitations and licensing information. Preview links are pinned to their exact version; the latest-release link is reserved for stable releases.

Verify a downloaded installer in PowerShell:

```powershell
Get-FileHash .\AGOT-Setup-x64.msi -Algorithm SHA256
```

Compare the complete hash with that release's checksum file. Inspect Properties → Digital Signatures, or use `Get-AuthenticodeSignature`, to check signing. An unsigned preview will be explicitly identified and may display Windows SmartScreen warnings. Do not assume an installer is signed.

## Source and licensing

This repository contains public distribution documentation and release metadata only. AGOT's application source remains private and is not supplied in GitHub's automatically generated source archives for this repository.

The repository's MIT license covers its public documentation and metadata; it does not license the separately distributed AGOT application or grant access to private source. Any installer must include its approved end-user terms and third-party notices. Required third-party source delivery is provided separately where applicable.

## Support

Website: [geotwins.org](https://geotwins.org) · Support: [admin@geotwins.org](mailto:admin@geotwins.org)

Report security concerns using [SECURITY.md](SECURITY.md). Automatic application updates are not enabled for the initial installer release.
