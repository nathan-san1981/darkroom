# Darkroom

A phone-first photo editor in a single HTML file, built as a stand-in for PicSay on iPhone. Everything runs in the browser; photos never leave the device.

**Use it:** https://nathan-san1981.github.io/darkroom/ — in Safari, tap Share → Add to Home Screen to run it full-screen like an app.

## Fun mode

Tap **Fun** in the header for a guided cut-and-paste flow:

1. **Cut:** pick a photo, roughly paint over (or loop around) what you want with ✨ Magic brush, which snaps to the real edges when you lift your finger, then tap Done.
2. **Place:** pick the photo to paste onto, or paste onto the same one. Saved cutouts stay in a tray.
3. **Adjust:** drag to move; drag the blue corner knob around to spin it about its center, or in and out to resize (pinch works too). Sliders for size, rotation, see-through (to check placement), and brightness to match the new photo. Flip, outline, shadow, nudge arrows, duplicate, send back, change background, save.

## Cut out (main tool)

- **✨ Magic brush (default):** roughly paint over what you want, or just draw a loop around its outline. When you lift your finger it snaps the selection to the object's actual edges, using color models and contrast-aware smoothing (a light GrabCut) run on the device with no download. **+ Add** grows it; **− Remove** paints over wrong bits and re-snaps. The brush size sets how far it searches for the edge. **✨ Snap to edges** refines a selection made with any other tool.
- **Tap select:** tap an object and it selects just that object, using the SlimSAM segmentation model (Segment Anything) run on-device via transformers.js. The model, about 15 MB, downloads from jsDelivr and Hugging Face on first use, then the browser caches it. **+ Add** and **− Remove** taps refine the selection. If the model can't load, Magic falls back to a color-based smart select with a Color range slider.
- **Brush / Eraser:** shade over what you want with your finger; erase to clean up edges. Brush size stays constant on screen, so pinch-zooming gives a finer brush.
- **Lasso:** trace around an area instead of painting it.
- **Undo stroke, Invert, Clear**, and an edge-softness slider for feathered edges.
- **With a selection:** paste as a movable layer, cut out & move (fills the hole), save to the cutouts tray, copy to clipboard, save as transparent PNG, erase from photo, or crop the photo to the shape.
- **Cutouts tray:** saved cutouts stay in the browser, so they can be pasted onto other photos. Pasted pieces can be moved, pinched to resize and rotate, flipped, outlined, shadowed, and blended.

## Everything else

| Tool | What it does |
|---|---|
| Adjust | Exposure, contrast, highlights, shadows, whites, blacks, clarity, sharpen, blur, grain, vignette, fade, levels, auto tone |
| Color | Temperature, tint, saturation, vibrance, 8-band HSL, color splash, split toning, duotone |
| Effects | 15 looks plus invert, sepia, posterize, solarize, pixelate, sketch, emboss, mirror, kaleidoscope, tint, tilt-shift |
| Crop | Free and fixed aspect crop, straighten, rotate, flip, resize |
| Retouch | Heal, clone, blur, sharpen, dodge, burn, saturate, desaturate, red-eye |
| Draw | Brush, marker, highlighter, eraser, arrows and shapes, pixelate/blur censor boxes |
| Text | 10 fonts, outline, shadow, background box, alignment, opacity, blend modes |
| Balloon | Speech, thought, shout and caption balloons with a draggable tail |
| Overlay | Image stickers, watermark, frames |

Also: layers panel, undo/redo, hold-to-compare, export as JPEG, PNG or WebP at a chosen size.

## Files

- `index.html` — the whole app (sample photos are embedded)
- `icon.png`, `apple-touch-icon.png` — home-screen icons

Sample photos are from scikit-image's bundled data set (public domain / CC0).
