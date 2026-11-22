# aion-build-assets

Public copies of third-party files that the aiOn app's builds depend on, kept here so a build does
not fail when the original download host is unavailable. Each file is used **only as a fallback**:
the build tries the original location first.

## onnxruntime-c 1.30.0 (iOS)

| | |
|---|---|
| File | `pod-archive-onnxruntime-c-1.30.0.zip` — release [`onnxruntime-c-1.30.0`](../../releases/tag/onnxruntime-c-1.30.0) |
| SHA-256 | `43f5d537c9a7253f2bead5853b868498546ba47880c59e05b1f8c8d7cf4efa90` |
| Original | `https://download.onnxruntime.ai/pod-archive-onnxruntime-c-1.30.0.zip` (Microsoft, [ONNX Runtime](https://github.com/microsoft/onnxruntime)) |
| Licence | MIT — [third-party/onnxruntime/LICENSE](third-party/onnxruntime/LICENSE) (also inside the zip) |

**What it is.** The files of Microsoft's CocoaPods archive for `onnxruntime-c` 1.30.0 (`Headers/`,
`LICENSE`, `onnxruntime.xcframework`), unmodified, re-zipped from a CocoaPods cache that downloaded
them from the original URL on 2026-10-07. The archive itself is a repackaging, so its checksum differs
from Microsoft's zip; the files inside are the same.

**Why.** On 2026-11-22 the original host served a certificate for `*.azureedge.net` instead of
`download.onnxruntime.ai`, so every download failed and iOS builds stopped.

**Not yet verified** byte-for-byte against Microsoft's archive (the original host was unavailable when
this copy was made). Compare each file's hash once it is back.
