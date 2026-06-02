# gsl3670-firmware

Firmware blob for the GSL3670 touchscreen controller.

The GSL3670 capacitive touch controller has no on-chip non-volatile firmware; a
firmware image must be uploaded to it over I²C every time it powers up. This
repository hosts those firmware blobs so they can be downloaded and cached at
build time by the ESPHome [`gsl3670`](https://esphome.io) touchscreen platform
instead of being vendored into the ESPHome source tree.

## Artifacts

Each firmware blob is published as a release asset, together with a `.sha256`
sidecar containing its SHA-256 checksum (standard `shasum -c` format).

| File | Device |
|------|--------|
| `seeed-d1001-fw.bin` | [Seeed Studio reTerminal D1001 (display module)](https://github.com/Seeed-Studio/reTerminal-D1001) |

## Verifying a download

```sh
shasum -a 256 -c seeed-d1001-fw.bin.sha256
```

## License

See [LICENSE](LICENSE).

