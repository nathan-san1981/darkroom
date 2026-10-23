# Darkroom

A phone-first photo editor in a single HTML file, built as a stand-in for PicSay on iPhone. Everything runs in the browser; photos never leave the device.

**Use it:** https://nathan-san1981.github.io/darkroom/ — in Safari, tap Share → Add to Home Screen to run it full-screen like an app.

## Cut out (main tool)

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
