# Libertinus Serif (self-hosted webfont)

Drop the four font files below into this directory. WOFF2 is preferred for
size; OTF is the fallback in `_sass/_libertinus.scss`.

Required filenames:

- `LibertinusSerif-Regular.woff2`   (or `.otf`)
- `LibertinusSerif-Italic.woff2`    (or `.otf`)
- `LibertinusSerif-Bold.woff2`      (or `.otf`)
- `LibertinusSerif-BoldItalic.woff2` (or `.otf`)

## Where to get them

Official release zips:
<https://github.com/alif-type/libertinus/releases>

The OTFs are inside the release zip. To convert OTF → WOFF2 (recommended for
production), use one of:

```bash
# Python (fonttools + brotli)
pip install fonttools brotli
pyftsubset --flavor=woff2 LibertinusSerif-Regular.otf

# Or woff2_compress (Google's reference tool)
woff2_compress LibertinusSerif-Regular.otf
```

Until the files are dropped here, the page falls back to Linux Libertine /
Georgia / Times automatically.
