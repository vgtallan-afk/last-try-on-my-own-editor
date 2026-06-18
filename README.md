# HTML Editor - Stability Final

This is a stability/performance pass.

Main fixes:
- Prevents iframe editor event listeners from accumulating after undo/load/reinject.
- Prevents autosave from serializing the entire page on every tiny mutation.
- Stops MutationObserver from watching style attributes on editor overlays.
- Replaces full sidebar rebuilds on every click with lazy/visible-panel refreshes.
- Reduces expensive color detection frequency.
- Removes full-width layout normalization from every commit/autosave.
- Reduces undo history memory pressure.
- Makes duplicate safer for grouped/multi-selected elements.
- Cleans cloned group metadata so duplicated groups do not corrupt the original group.
- Keeps previous device-specific background/gradient, move handle, carousel, ZIP import/export, and autosave features.

Recommended workflow:
1. Upload this ZIP to GitHub/Vercel.
2. Open the editor.
3. Import your existing Project ZIP.
4. Continue editing.
