# Image Squeezer

Image Squeezer is a portable, single-file HTML5 application that compresses images directly in your browser. Process images in batches, download a ZIP archive, or replace supported original files with smaller versions.

[Live application](https://firerayo.github.io/Image-Squeezer/)

## Features

- **Batch input:** Select images with the file picker or drag and drop them. Remove individual files or clear the list.
- **Size target:** Set the desired final size from 1% to 100% of each original file, using a number field or slider.
- **Adaptive compression:** The app tries different encoding quality levels. Enable **Reduce resolution if needed** to allow smaller image dimensions.
- **Input formats:** JPG/JPEG, PNG, WebP, GIF, BMP, AVIF, SVG, and other image types your browser can decode.
- **Output formats:** Choose **Automatic**, **JPEG**, **WebP**, or **PNG**. Available encoders depend on the browser.
- **ZIP output:** Select **Download ZIP archive** to export the batch without modifying the originals. Output filenames are made unique.
- **In-place output:** Select **Overwrite original images** to replace static JPEG, PNG, or WebP files. This mode requires a compatible file picker, write permission, and confirmation. It preserves filenames and formats, and skips files that cannot be made smaller.
- **Progress and control:** View per-file outcomes, file sizes, target status, batch progress, and totals. Cancel processing or review individual errors.
- **Interface:** Switch between Light and Dark themes and four languages: English, Spanish, Italian, and Brazilian Portuguese. Open **About** for version and author information.

## Quick start

No installation, account, server, or external library is required.

1. Download [`index.html`](index.html) from this repository.
2. Open the file in a modern browser.
3. Under **01 Select images**, choose your files or drag them into the selection area.
4. Under **02 Adjust compression**, set **Final file size percentage** and choose the output format.
5. Under **03 Save results**, leave **Download ZIP archive** selected.
6. Click **Compress and save images** to process the batch and download the ZIP file.

**Example:** Select ten JPEG images, set the target to 50%, and keep **Automatic** selected. The app attempts to reduce each image to half its original byte size. Actual results can vary.

To replace files instead, select **Overwrite original images**. Use **Select original images with write access** to choose the originals again. Click **Compress and save images**, then confirm the overwrite and grant permission. **Back up important images first.** Successfully processed files are replaced individually; this action has no undo feature.

## Limitations and compatibility

- The size percentage is a target, not a guarantee. The app can retain the original if no smaller result is available.
- File decoding and JPEG/WebP encoding depend on browser support. HEIC/HEIF and TIFF input may not work in every browser.
- Overwriting requires the browser's File System Access picker (`showOpenFilePicker`). Use a compatible desktop browser, such as Chrome or Edge.
- Overwrite mode rejects unsupported formats and animated PNG or WebP files. A 100% target does not overwrite originals.
- Re-encoding can remove metadata, including EXIF data and color profiles. Animated images and SVG content become static raster images when re-encoded.
- The ZIP writer uses ZIP32 limits. The app accepts up to 2,000 selected images per batch.

## Data and privacy

Images are processed locally. The application contains no upload service, analytics, or tracking requests. Files remain on your device unless you choose to share them separately.

The browser's `localStorage` saves language and theme preferences when permitted. It does not store your selected image files. Output is saved as a downloaded ZIP or, after confirmation, written over selected originals. The optional GitHub link in **About** opens an external website only when selected.

## Development and tests

The HTML, CSS, JavaScript, translations, and icons are contained in [`index.html`](index.html). Edit this file directly and reload it in a browser. The repository has no build step, package dependencies, automated test suite, or configured continuous integration workflow.

## Contributing and support

Use [GitHub Issues](https://github.com/FireRayo/Image-Squeezer/issues) to report defects or request changes. Submit code changes through [pull requests](https://github.com/FireRayo/Image-Squeezer/pulls).

## License and credits

Licensed under the **GNU General Public License, version 3 (GPLv3)**. Read the full terms in [`LICENSE`](LICENSE).

Created by **Raymundo Ortiz (FireRayo)**. Source code: [FireRayo/Image-Squeezer](https://github.com/FireRayo/Image-Squeezer).
