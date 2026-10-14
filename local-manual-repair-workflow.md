# Local manual repair workflow

Use this checklist for a small visible text label, logo, or piece of clutter on an image you are allowed to edit.

1. Keep a copy of the original image before making changes.
2. Select a JPG, PNG, or WebP file from your device.
3. Mark only the visible area you intend to repair. Avoid nearby details you need to preserve.
4. Repair a small area and inspect the result before downloading.
5. If a face, edge, lettering, or repeated pattern changes, clear the mark and retry with a tighter selection.
6. Export the reviewed result as PNG.

## How the repair is produced

The marked pixels are replaced with a weighted average of nearby unmarked pixels, sampled outward from each masked pixel until enough unmasked neighbours are found. That makes the result repeatable: the same mask on the same image gives the same output. It also means the tool has nothing to invent — it continues whatever is already next to the mark.

## Fit and limits

This workflow is most suitable for a small mark on a comparatively even background. It is not automatic detection, and it does not guarantee a seamless reconstruction on detailed textures, faces, or large areas.

Measured limits of the documented workflow: one image per run, up to 8 MiB, longest side up to 4096 px, brush from 8 to 100 px. Export is always PNG. See `image-format-export-matrix.csv`.

## Privacy boundary

In the documented workflow, image processing occurs in the browser rather than by uploading the selected image to the tool's processing server.
