# Changelog

## v3.9 — Typed Screenshot Only
- Removed image/diagram cropping, visual-region detection, crop attachment, reference screenshot upload, image positioning and diagram-colour controls.
- Reframed OCR UI and prompts for computer-typed screenshots rather than handwritten-photo extraction.
- Preserved local OCR, optional Gemini OCR, editable OCR result, insert-to-solution workflow, watermark, pagination and JPG export.
- Maths typesetting is **not yet fully fixed**: the renderer remains Canvas-based and only normalizes common LaTeX to readable text notation.

## Verification
- Inline JavaScript syntax checks passed.
- Browser end-to-end rendering and live Gemini API request were not tested here.


## v4.1 — Watermark Sliders & Compact Font Preview
- Replaced watermark position, size, and opacity dropdowns with live sliders.
- Horizontal and vertical position sliders cover the full 0–100% page range.
- Logo size slider covers 5–80% of page width; opacity slider covers 1–30%.
- Reduced font candidate previews to a compact fixed-height preview to avoid excessive vertical space.
- Reset formatting now restores watermark slider defaults (center, 35% width, 6% opacity).

## Verification
- Inline JavaScript syntax checks passed for both HTML entry points.
- ZIP integrity checked after packaging. Browser end-to-end rendering has not been independently verified.

## v4.4 — Remove Layout Controls
- Removed the Page size, Line spacing, and Text width controls from the interface.
- Rendering now uses fixed defaults for those settings; font size remains controlled by its existing dropdown and slider.
- Watermark controls and other workflows are unchanged.
- Static JavaScript syntax and ZIP integrity checks passed; browser end-to-end testing remains pending.


## v4.8 — Independent Page Dimension Fix
- Fixed horizontal resizing so it changes the output canvas width and the review preview width, not only the height.
- Vertical slider changes only the output canvas height.
- Removed canvas-context scaling so text and watermark are not scaled when page dimensions change.
- Both dimensions remain independent; output may clip content if the user makes the page smaller than its fixed-size content.


## v4.9 — Expanded Solution Text Size Range
- Expanded solution text size slider from 18–52 px to 8–100 px.
- Added dropdown presets for very small through very large text sizes.
- Kept the existing font-size value as the source of truth; page dimensions and watermark controls are unchanged.
- Static JavaScript syntax and ZIP integrity checks run during packaging; browser end-to-end rendering remains unverified.


## v4.11.1 — Compact font preview
- Reduced font preview canvas height by 50% and tightened its top spacing.
- Kept preview font selection, slider range, solution font size, watermark, page sizing, and other behavior unchanged.


## v4.12 — Remove Gemini feature
- Removed Gemini Vision OCR UI, API-key input, model selector, external API request code, and related status handling from both HTML builds.
- Kept local Tesseract screenshot OCR and the rest of the tool unchanged.


Version 4.16: Removed only the Preview text size control and obsolete handlers. Preview font dropdown and other features are retained.


## v4.19 — Professional Studio (cosmetic only)
- Added navy/blue top navigation with links to existing sections.
- Reorganized the existing editor and settings into a desktop 65/35 split.
- Moved the existing rendered-page preview area into a full-width panel below.
- Preserved existing feature/control IDs and application processing JavaScript.


## v4.20 — Sticky Settings Studio
- Made the existing Settings panel sticky on desktop so it remains accessible while reviewing rendered pages.
- Kept the panel in normal flow on narrow/mobile layouts.
- CSS/layout only; application JavaScript and existing control IDs unchanged.


## v4.21
- Added an upper-right expand control to every rendered page card.
- Added a large preview dialog with fit-to-window and 50%–300% zoom controls.
- Preserved the source canvas and existing approval/download workflow.


## v4.23 — Premium Blue Studio theme
- Visual-only refresh: brighter blue actions, soft blue-white surfaces, refined borders, shadows and typography.
- Preserved existing layout, controls, page preview/zoom, dark-theme toggle and application logic.


## v4.24 — Reference Theme Applied
Applied the supplied Premium Blue Studio visual reference using CSS-only styling. Existing layout, controls, IDs, application JavaScript, and dark-theme toggle behavior are preserved.


## v4.25 — Canvas Maths Rendering
- Added canvas-drawn stacked fractions, square roots, superscripts, subscripts, and common maths operators for rendered pages and JPG output.
- Kept normal explanatory text on the selected font and preserved the existing page/layout workflow.
- This is a lightweight renderer for common notation, not a full LaTeX engine; unsupported advanced LaTeX may still need manual simplification.


## v4.25.1 — OCR maths capture improvement
- Added a Math / equation image-preparation option using 3× enlargement and stronger grayscale contrast.
- Math mode uses single-line OCR and preserves inter-word spacing to improve capture of small powers, roots and symbols.
- Existing editor, rendering, theme, zoom, watermark and export workflow retained.
- OCR remains probabilistic; verify every exponent, radical and sign against the source image.


## v4.25.2 — SSC WARS header cleanup
- Added “By SSC WARS Team” beneath the main header.
- Removed the technical version banner and local-processing implementation note from the interface.
- No application controls or processing logic intentionally changed.
