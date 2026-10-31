# ImageSqueezer

![Version 1.7](https://img.shields.io/badge/version-1.7-2563eb?style=plastic&labelColor=555) ![HTML5 single-file](https://img.shields.io/badge/HTML5-single--file-f97316?style=plastic&labelColor=555) ![Offline ready](https://img.shields.io/badge/offline-ready-279653?style=plastic&labelColor=555) ![Portable](https://img.shields.io/badge/portable-yes-1688ae?style=plastic&labelColor=555) ![Tracking-free](https://img.shields.io/badge/tracking-free-279653?style=plastic&labelColor=555) [![License GPLv3](https://img.shields.io/badge/License-GPLv3-2563eb?style=plastic&labelColor=555)](LICENSE)

ImageSqueezer compresses images in your browser. Download results as a ZIP or overwrite supported original files.

## Live application:

[https://firerayo.github.io/ImageSqueezer/](https://firerayo.github.io/ImageSqueezer/)

## Features

- **Image selection:** Choose or drag images in ZIP mode. Review names, sizes, and results. Remove files or clear the list.
- **Input formats:** Select JPEG, PNG, WebP, GIF, BMP, AVIF, SVG, TIFF, HEIC, and HEIF. Decoding depends on browser support.
- **Batch processing:** Process up to 2,000 images sequentially. Monitor progress, errors, and sizes. Cancel processing.
- **Size target:** Choose 1% to 100% of each original file's size using the number field or slider.
- **Adaptive compression:** Search for suitable encoding quality. Enable **Reduce resolution if needed** to allow smaller image dimensions.
- **ZIP output formats:** Choose **Automatic**, **JPEG**, **WebP**, or **PNG**, subject to browser encoding support.
- **ZIP export:** Download one archive without changing source files. Duplicate output filenames are made unique. The archive uses `ImageSqueezer_v1.7_YYYY-MM-DD.zip`.
- **Original overwrite:** Select originals with write access and confirm. Eligible images replace the originals without changing names, locations, or formats.
- **Interface:** Switch between Light and Dark themes. Choose English, Spanish, Italian, or Brazilian Portuguese without reloading the page.
- **About:** View the application version, author, and GitHub repository link.

## Quick start

No installation, server, account, build step, or external library is required.

1. Download [`index.html`](index.html) from the repository.
2. Open the file in a modern browser.
3. Under **01 Select images**, choose files or drag images into the selection area.
4. Under **02 Adjust compression**, set the target percentage, output format, and resize preference.
5. Under **03 Save results**, select **Download ZIP archive**.
6. Click **Compress and save images**.
7. Save the downloaded ZIP file.

**Example:** Select ten JPEG images and set 50%. ImageSqueezer attempts to keep each file at half its original size. Results may vary.

**To overwrite originals:** Select **Overwrite original images**. Click **Select original images with write access** and choose the originals. Start processing, confirm the warning, and grant write permission if requested. Back up important files first. Successful reductions replace originals as each image finishes; there is no undo.

## Limitations and compatibility

- Size targets are not guaranteed. ZIP can retain originals; overwrite skips unchanged files.
- Browser support controls image decoding and encoding. TIFF, HEIC, and HEIF may not open in some browsers.
- ZIP32 limits archives to approximately 4 GiB. ZIP packaging adds no further image compression.
- Overwriting requires `showOpenFilePicker` and write permission. Use a compatible desktop browser, such as Chrome or Edge.
- Overwriting supports static JPEG, PNG, and WebP files only. Animated PNG/WebP, unsupported formats, and files without a size reduction are skipped.
- A 100% target does not modify originals. Re-encoding can remove Exchangeable Image File Format (EXIF) metadata and color profiles.
- Animated images and Scalable Vector Graphics (SVG) can become static raster images when re-encoded for ZIP output.

## Data and privacy

Images are processed locally without uploads, analytics, tracking, or required network resources. The **About** link opens GitHub only when clicked.

The browser stores language and theme preferences in `localStorage`, when available. It does not store selected images there. Output files are downloaded or written only with the required browser permissions.

## Development and tests

HTML, Cascading Style Sheets (CSS), JavaScript, icons, and translations are contained in [`index.html`](index.html). Edit it and reload the browser. No build scripts, package dependencies, or automated test workflows are configured. Test changes with backed-up images.

## Contributing and support

Report defects or suggest changes through [GitHub Issues](https://github.com/FireRayo/ImageSqueezer/issues). Submit code changes through [pull requests](https://github.com/FireRayo/ImageSqueezer/pulls).

## License and credits

Licensed under the **GNU General Public License, version 3 (GPLv3)**. See the complete [`LICENSE`](LICENSE).

Created by **Raymundo Ortiz (FireRayo)**. See the [source repository](https://github.com/FireRayo/ImageSqueezer).
