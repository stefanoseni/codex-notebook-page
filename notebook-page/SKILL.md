---
name: notebook-page
description: Lay out notes, schoolwork, math, or simple sketches on a ruled notebook page for copying by hand. Use when the user asks for notebook format, a paper-style answer, or says they need to write, copy, or draw the result by hand. Ordinary study questions and digital design sketches use their usual formats.
---

# Notebook Page

Make the rendered page the main answer. Put what belongs in the physical notebook on the page, in the order the user should write it. Keep any optional tutoring comments or source links outside the sheet unless they belong in the assignment. Follow the requested language, detail, and teaching mode.

- **Notes:** Use a short title, brief lines, and blank ruled space between ideas. Let longer text wrap naturally onto the rules. Preserve required wording and facts.
- **Math:** Set one meaningful step per line. Align related work, stack fractions or arithmetic where appropriate, and use normal written notation for powers, roots, and units. For a practice problem, leave ruled working space and reveal the solution only when requested. If the user wants hints, put the current hint or partial setup on the page.
- **Sketches:** Draw the actual diagram on the page. Use easy-to-copy strokes, a few labels and, for graphs, the scale, axes, and points needed to reproduce it. Use squared paper for coordinate plots. Fit long answers across pages instead of shrinking the writing.

## Render the page

Start from [the ruled page template](assets/notebook.html). Replace its sample content and use a unique root ID, updating the scoped styles to match. Keep the margin and faint lines. Add a blank row with an empty `p` element and use `class="block"` on content with its own height, such as a figure or a row with a tall formula. Use real MathML for typeset math and an accessible line drawing for spatial content. Keep essential details legible on narrow screens.

When the inline visualization surface is available, follow its output contract and put the rendered page directly in the reply. Otherwise, wrap the fragment in a complete standalone HTML document and link the file. The template has fallbacks for use outside the inline surface and a print stylesheet. Use the standalone page or an available document renderer for a requested print file.

Check the rendered text, notation, and diagram against the request. If the surface or renderer fails and a file is unavailable, provide a compact notebook-ready answer in chat using separate lines, rendered math, and short drawing directions as needed.
