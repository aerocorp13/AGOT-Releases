# AGOT Desktop — responsible security disclosure

Report a suspected AGOT installer, desktop, data-permission, GeoAI tool-execution or model credential vulnerability **privately** to [admin@geotwins.org](mailto:admin@geotwins.org) with subject **AGOT security report**.

Include the exact affected product version/tag, Windows version, expected vs observed access or behavior, impact and minimal safe reproduction steps. Do not send real customer datasets, access tokens, passwords, personal information or source archives in ordinary email; coordinate a secure transfer if absolutely necessary.

## Current distribution and supported channels

AGOT Desktop has published **Preview 1 (1.0.0), Preview 2 (1.0.1) and Preview 3 (1.0.2)** Windows MSI assets; all are **pre-release evaluation builds**. Publication does not imply a security certification, defined support SLA or a guarantee that older previews will receive fixes. The [latest published release](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.1-preview.3) and its limitations determine what is being distributed now.

Download only through this repository's [GitHub Releases](https://github.com/aerocorp13/AGOT-Releases/releases) or [GeoTwins Africa](https://geotwins.org/agot/). Compare the asset's GitHub SHA-256 digest where available; check the actual signing status separately. A matching hash is not equivalent to code signing or proof that a binary is safe.

## Experimental 1.0.4 and GIS-host caveats

The 1.0.4 MSI was reported as **NotSigned** at packaging and is not a certified automatic updater. Experimental QGIS/ArcGIS packages require a working local AGOT service, authorization, explicit operator approval and licensed source rights. Never record AGOT_HOST_TOKEN or QGIS session bearers in GIS project histories, screenshots or public issue reports. See [preview acceptance](docs/previews/PREVIEW_ACCEPTANCE_20261105.md).

## High-impact areas

Please report unsafe cross-user/tenant data access, historical World source permission bypass, unauthorized side-effect execution, private model credential disclosure, forged/replayed action receipts, insecure updates/installers, malicious plugins or unsafe external data fetches.

Do not perform destructive testing against other users or production systems. Do not publish proof-of-concept exploit details before private coordination.

We aim to triage reports responsibly but do **not** promise a fixed response time or bug-bounty reward.

Other problems can be reported through sanitized [GitHub Issues](https://github.com/aerocorp13/AGOT-Releases/issues). Installation and integrity guidance: [docs/INSTALLATION.md](docs/INSTALLATION.md).
