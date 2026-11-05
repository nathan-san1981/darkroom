# Darkroom

A free photo app for iPhone: paint over anything to cut it out, drop it onto another photo, and add captions, speech bubbles or your own writing. It runs in the browser, works offline once installed, and your photos never leave your phone.

![Darkroom](preview.png)

## Get it

1. On your iPhone, open **https://nathan-san1981.github.io/darkroom/** in **Safari**.
2. Tap **Share**, then **Add to Home Screen**.

Darkroom then opens from its own icon, full-screen like any other app. (It also works in Chrome or on Android, just without the Home Screen step being quite as smooth.)

## How it works

Darkroom is built around one thing: putting part of one photo onto another. Four steps run along the bottom:

1. **Photo.** Pick your main photo.
2. **Add.** **Put another photo on top.** It starts half see-through, so you can see both photos at once. Or **cut something from another photo**: paint over the part you want and it drops onto your main photo. Saved cutouts and pasted images can be added from here too.
3. **Adjust.** The **See-through** slider (plus Solid / Half / Faint) sets how much of the top photo shows. Switch your finger to **Erase** to rub away parts of the top photo and show the one underneath; erased parts show faintly while you work. **Restore** paints them back, **⇄ Reverse** flips what's erased and what's kept, and **Keep only…** hides everything so you paint in just the part you want. In **Move**, drag to position it and use the blue corner knob to spin and resize.
4. **Text.** Comic bubbles in one tap: speech, puffy thought clouds, spiky shout, dashed whisper, yellow caption boxes and a POW! sound effect, in real comic lettering. Plus captions in one-tap styles, writing with your finger, and Paint over / Cover box to hide things first.

Then tap **Save picture**. On iPhone the share sheet opens, so choose **Save Image** to put it in Photos.

Need more? **More tools** at the top opens the full editor: exposure and color, filters and looks, crop and straighten, heal and clone, drawing and shapes, frames, layers, and export as JPEG, PNG or WebP.

Your work is saved as you go. If iPhone reloads the page while you're in another app, tap **Continue editing** to pick up where you left off.

## Privacy

Everything happens on your phone. Photos aren't uploaded anywhere, and there are no accounts or ads. The only things downloaded are the app itself, its fonts, and (only if you use **Tap select** in the editor) a small AI model.

---

### Technical notes

- `index.html` is the whole app: plain HTML, CSS and JavaScript, no build step. Sample photos are embedded.
- `manifest.webmanifest` and `sw.js` make it installable and offline-capable. Bump `CACHE` in `sw.js` on each release so installed copies update.
- `icon.png`, `apple-touch-icon.png` are the Home Screen icons; `preview.png` is the link-preview card.
- Magic brush is an on-device GrabCut-style segmentation (color models plus contrast-aware smoothing). Tap select uses SlimSAM via transformers.js, loaded from jsDelivr and Hugging Face on first use, with a color-based fallback.
- Sample photos are from scikit-image's bundled data set (public domain / CC0).
