# segmentation_hd.tflite

Full U²-Net salient-object segmentation model.

- Source: U²-Net by Xuebin Qin et al., https://github.com/xuebinqin/U-2-Net, licensed under the Apache License 2.0 (full text in `LICENSE`).
- Weights obtained as `u2net.onnx` from the rembg project's GitHub release v0.0.0 (rembg is MIT licensed), MD5 `60024c5c889badc19c04ad937298a77b`, which matches the checksum published in rembg's source. All 231 weight tensors of that file are bit-identical in the file this model was converted from.
- Changes made (Apache-2.0 section 4b): converted ONNX to TensorFlow Lite with onnx2tf, quantised weights to float16, and trimmed the graph to the single fused output.
- Input `[1,320,320,3]` float32, output `[1,320,320,1]` float32 (sigmoid).
- File: 88,085,892 bytes, SHA-256 `7b898381005a2f6efb931f4cd59ec4f1ba7e806a12e9feb6b9efb504b92b556b`.
