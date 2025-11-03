# Chrome PDF Dark Mode Bookmarklet Builder

This project provides a small web app that helps you generate a Chrome bookmarklet for viewing PDF files in a dark theme. The generator exposes sliders for inversion, hue rotation, sepia, brightness, contrast, and saturation so you can find a dark mode combination that fits your eyes before saving it as a bookmarklet.

## Using the generator (Chrome desktop)

Quick steps for Chrome on desktop:

1. Go to https://ingbunga.github.io/chrome-pdf-darkmode-bookmarklet-builder/
2. Tweak the sliders until the preview looks good to you.
3. Click Copy Bookmarklet to copy the `javascript:` code to your clipboard.
4. Create a bookmark and paste the code:
   - Show the Bookmarks Bar (Ctrl+Shift+B), right‑click it, choose Add page…, give it a name, and paste the copied `javascript:` code into the URL field. Save.
   - Alternative: Open Bookmark Manager (Ctrl+Shift+O) → Add new bookmark → paste the `javascript:` code into the URL field.
5. Open any PDF in Chrome and click the bookmark to apply dark mode. Click it again to toggle off.


## How it works

The bookmarklet injects (or removes) a `<style>` tag that targets the Chrome PDF viewer container (`html[data-pdf-viewer-done="true"]`) and the embedded PDF element (`body > embed[type="application/pdf"]`). The generated CSS applies your chosen filter chain and background color, and optionally enforces `color-scheme: dark` so the viewer chrome inherits a dark palette.

