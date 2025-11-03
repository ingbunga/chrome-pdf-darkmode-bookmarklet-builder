# Chrome PDF Dark Mode Bookmarklet Builder

This project provides a small web app that helps you generate a Chrome bookmarklet for viewing PDF files in a dark theme. The generator exposes sliders for inversion, hue rotation, sepia, brightness, contrast, and saturation so you can find a dark mode combination that fits your eyes before saving it as a bookmarklet.

## Using the generator


## How it works

The bookmarklet injects (or removes) a `<style>` tag that targets the Chrome PDF viewer container (`html[data-pdf-viewer-done="true"]`) and the embedded PDF element (`body > embed[type="application/pdf"]`). The generated CSS applies your chosen filter chain and background color, and optionally enforces `color-scheme: dark` so the viewer chrome inherits a dark palette.

The repository still includes `bookmarklet.js`, which shows the original static style for reference. The generator produces the same pattern, but with your custom values.
