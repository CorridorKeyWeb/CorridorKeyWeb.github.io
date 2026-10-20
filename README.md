# CorridorKey 2.0 Studio

A single-file, in-browser front end for CorridorKey 2.0, the green-screen keying model from Corridor Digital.

This version is configured for the 2.66 GB `.safetensors` checkpoint at:

https://huggingface.co/nikopueringer/CorridorKey2.0/resolve/main/corridorkey_v2.safetensors

## Quick start

1. Open the page in Chrome or Edge. WebGPU needs HTTPS or `localhost`.
2. Click Import media and load a photo or video.
3. Under Model & performance, click Load .safetensors and choose `corridorkey_v2.safetensors`, or open the page with:

```text
?model=https://huggingface.co/nikopueringer/CorridorKey2.0/resolve/main/corridorkey_v2.safetensors
```

4. Pick a preset and process the current frame.
5. Export the result as PNG or MP4.

## Model download

The model is large: `corridorkey_v2.safetensors` is about 2.66 GB.

Use one of these paths:

- Direct from Hugging Face:
  https://huggingface.co/nikopueringer/CorridorKey2.0/resolve/main/corridorkey_v2.safetensors
- Or use the repo UI and browse to the model file in the Hub.

For local use in a Git repo, track the file with Git LFS:

```bash
git lfs install
git lfs track "*.safetensors"
git add .gitattributes
git add corridorkey_v2.safetensors
git commit -m "Add CorridorKey 2 model"
git push
```

## Browser requirements

- Desktop Chrome or Edge is recommended.
- WebGPU is preferred.
- A large amount of free RAM is required for a 2.66 GB checkpoint. Expect a heavier load than the original v1 model.
- If the model is too large for your browser session, use the `?model=` URL and keep the file downloaded once, or use a local copy in the same origin.

## Notes

- The generated hint is only a rough guide; better hints produce cleaner results.
- For the cleanest key, use your own alpha hint when available.
- Video is processed frame-by-frame.

## Credits and license

CorridorKey is by Corridor Digital. Check the original model license and usage terms before sharing or redistributing any converted model files.
