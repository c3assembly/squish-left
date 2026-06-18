# vertical-static-image-app

Turns a vertical image into a 1920×1080 (16:9) static image for ATEM.

**Live app:** https://c3assembly.github.io/vertical-static-image-app/

## What it does

A single static web page that runs entirely in your browser (no server, no
upload — the image never leaves your machine):

1. Accepts a **PNG or JPG** (ideal input **1344×840**; any **8:5 / 1.6** aspect
   ratio works).
2. Resizes it to **675×1080**.
3. Composites it onto a **1920×1080** black frame, anchored to the **left** edge
   (the rest of the frame stays black).
4. Exports a downloadable **1920×1080 PNG**.

If the input's aspect ratio isn't 8:5, it still produces output but shows a
warning (the image will be stretched to 675×1080).

## Usage

Just open the live app and drop in an image, then click **Download PNG**.

To run locally, open `index.html` directly in any modern browser — there's no
build step or dependencies.

## Deployment

Pushing to `main` triggers the
[`Deploy to GitHub Pages`](.github/workflows/deploy-pages.yml) workflow, which
publishes the site automatically.

> **One-time setup:** In the repo's **Settings → Pages**, set
> **Source = "GitHub Actions"**. After that, every push to `main` deploys.
