# OpenNess Vulnerability Scanner releases

Installers of the [OpenNess Vulnerability Scanner](https://getopenness.com) desktop app and the
signed update manifest the app reads. There is no source code here; every release is published
by the release workflow of the [openness-desktop](https://github.com/s4e-io/openness-desktop)
repository.

| File | Platform |
|---|---|
| `OpenNess-Desktop-<version>.pkg` | macOS (Apple silicon and Intel), signed with Developer ID and notarized |
| `OpenNess-Desktop-<version>-setup.exe` | Windows 10, 11 and Server 2019+ (amd64), signed |
| `manifest.json` | The update manifest: `{payload, sig}`, Ed25519 signed |
| `SHA256SUMS` | Checksums of every file in the release |

Verify a download:

```sh
shasum -a 256 -c --ignore-missing SHA256SUMS
```

Each release bundles the [openness-collector](https://github.com/s4e-io/openness-collector) and
[openness-resolver](https://github.com/s4e-io/openness-resolver) versions it was tested with;
the release notes name them.
