# Travel Gallery — model mirror

Backup copies of the third-party files that [Travel Gallery](https://gallery.kwappy.com) downloads on demand for
**search by photo content** (Windows server and Android app). The apps download them from the original sources first
and fall back to this mirror only when an original is gone. Every file is checked against its SHA-256 before use,
so a file from here is byte-for-byte the same as the original.

The files are attached to the release [`v1`](../../releases/tag/v1). They are unmodified copies — nothing here was
trained, converted or changed by us.

| File | Size (bytes) | Original source (pinned commit) | Licence |
|---|---:|---|---|
| `siglip2-vision.onnx` | 371 992 072 | [onnx-community/siglip2-base-patch16-256-ONNX](https://huggingface.co/onnx-community/siglip2-base-patch16-256-ONNX) `onnx/vision_model.onnx` @ `d1114256522a37ffa257a0a58017348ab0058db2` | Apache 2.0 (model: [google/siglip2-base-patch16-256](https://huggingface.co/google/siglip2-base-patch16-256)) |
| `siglip2-text.onnx` | 283 438 275 | same repository, `onnx/text_model_quantized.onnx` | Apache 2.0 |
| `siglip2-tokenizer.model` | 4 241 003 | same repository, `tokenizer.model` | Apache 2.0 |
| `opus-pl-en-encoder.onnx` | 52 095 390 | [Xenova/opus-mt-pl-en](https://huggingface.co/Xenova/opus-mt-pl-en) `onnx/encoder_model_quantized.onnx` @ `aeaf0e003b045248c28a559a5ce6027b54ebdaba` | Apache 2.0 (model: [Helsinki-NLP/opus-mt-pl-en](https://huggingface.co/Helsinki-NLP/opus-mt-pl-en)) |
| `opus-pl-en-decoder.onnx` | 59 031 466 | same repository, `onnx/decoder_model_quantized.onnx` | Apache 2.0 |
| `opus-pl-en-source.spm` | 834 921 | same repository, `source.spm` | Apache 2.0 |
| `opus-pl-en-target.spm` | 785 212 | same repository, `target.spm` | Apache 2.0 |
| `opus-pl-en-vocab.json` | 1 642 111 | same repository, `vocab.json` | Apache 2.0 |
| `onnxruntime.dll` | 12 418 080 | NuGet [Microsoft.ML.OnnxRuntime 1.22.0](https://www.nuget.org/packages/Microsoft.ML.OnnxRuntime/1.22.0), `runtimes/win-x64/native/onnxruntime.dll` | MIT (Microsoft) |

Checksums: [`SHA256SUMS`](SHA256SUMS). Licence texts: [`licenses/`](licenses) — Apache License 2.0, the ONNX Runtime
licence and its third-party notices (from the same NuGet package).

Credits: SigLIP 2 — Google (Tschannen et al., 2025); OPUS-MT — Helsinki-NLP, University of Helsinki
(Tiedemann & Thottingal, 2020); ONNX conversions — onnx-community and Xenova (Hugging Face); ONNX Runtime — Microsoft.
