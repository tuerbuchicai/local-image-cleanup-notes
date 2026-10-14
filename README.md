# Local Image Cleanup Notes

A small reference pack for repairing one small visible mark in an image you are allowed to edit, using a browser-based workflow that does not upload the image anywhere.

For the working browser tool, see [Local Watermark Cleanup](https://localwatermarkcleanup.com/).

## Files

- `site-page-map.csv` — every page on the site, grouped by what it covers.
- `image-format-export-matrix.csv` — accepted inputs, fixed export format, and the real limits.
- `local-manual-repair-workflow.md` — a repeatable small-area repair checklist.
- `repair-verification-checklist.md` — what to check before you repair, and what to check after.
- `visible-and-invisible-mark-boundaries.md` — what this workflow can and cannot address.

## What the workflow does, mechanically

The tool paints a mask over the area you select, then replaces each masked pixel with a weighted average of nearby unmasked pixels. It is deterministic, it runs in the browser tab, and it makes no network request. There is no model guessing what was underneath.

## Scope

This is not an automatic detection system, an ownership registry, or a method for altering invisible provenance signals. Use it only with images you own or have permission to edit.

Last updated: 2026-10-13.
