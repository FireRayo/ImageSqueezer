
# ImageSqueezer

![Version 1.6](https://img.shields.io/badge/version-1.6-2563eb?style=plastic&labelColor=555) ![HTML5 single-file](https://img.shields.io/badge/HTML5-single--file-f97316?style=plastic&labelColor=555) ![Offline ready](https://img.shields.io/badge/offline-ready-279653?style=plastic&labelColor=555) ![Portable](https://img.shields.io/badge/portable-yes-1688ae?style=plastic&labelColor=555) ![Tracking-free](https://img.shields.io/badge/tracking-free-279653?style=plastic&labelColor=555) [![License GPLv3](https://img.shields.io/badge/License-GPLv3-2563eb?style=plastic&labelColor=555)](LICENSE)

ImageSqueezer reduces image file sizes locally in your browser. Process batches, download a ZIP archive, or overwrite supported original files.

## Live application:

[https://firerayo.github.io/ImageSqueezer/](https://firerayo.github.io/ImageSqueezer/)

## Features

- **Image selection:** Choose files or drag and drop them. Review filenames and sizes, remove files, or clear the list.
- **Input formats:** Select JPEG, PNG, WebP, GIF, BMP, AVIF, SVG, TIFF, HEIC, and HEIF files. Decoding depends on browser support.
- **Batch processing:** Process up to 2,000 images sequentially. View results, errors, progress, and size totals. Cancel processing.
- **Size target:** Set 1% to 100% of the original size with a number field or slider.
- **Adaptive compression:** Adjust encoding quality automatically. Enable **Reduce resolution if needed** to allow dimension changes.
- **Output formats:** Choose **Automatic**, **JPEG**, **WebP**, or **PNG** for ZIP output, subject to browser encoding support.
- **ZIP export:** Download results in one ZIP file without changing originals. Output filenames are unique.
- **Original overwrite:** Replace supported original files in place after confirmation and write authorization.
- **Interface:** Choose Light or Dark theme and English, Spanish, Italian, or Brazilian Portuguese. Language changes need no reload.
- **About:** View the application version, author, and GitHub link.

## Quick start

No installation, server, account, build step, or external library is required.

1. Download [`index.html`](index.html) from this repository.
2. Open it in a modern browser.
3. Under **01 Select images**, choose images or drag them into the selection area.
4. Under **02 Adjust compression**, set the target percentage and output format.
5. Under **03 Save results**, select **Download ZIP archive**.
6. Click **Compress and save images**.
7. Save the downloaded ZIP file.

**Example:** Select ten JPEG files and set 50%. The application attempts to halve each file size; results may vary.

**To overwrite originals:** Choose **Overwrite original images**. Click **Select original images with write access** and select the originals. Start compression. Confirm the warning. Grant write permission if requested. **Back up important files first.** Successful results replace originals individually; there is no undo.

## Limitations and compatibility

- The size target is not guaranteed. The app retains the original if a smaller result is unavailable.
- Browser support determines input decoding and JPEG/WebP encoding. Some TIFF or HEIC/HEIF images may not open.
- ZIP32 limits the archive to approximately 4 GiB. ZIP packaging does not further compress images.
- Overwriting requires `showOpenFilePicker` and write permission. Use a compatible desktop browser, such as Chrome or Edge.
- Overwrite supports static JPEG, PNG, and WebP. It preserves names and formats and skips files that do not shrink.
- Overwrite skips animated PNG/WebP. A 100% target leaves originals unchanged.
- Re-encoding may remove Exchangeable Image File Format (EXIF) metadata and color profiles. Animated images and SVG may become static raster images.

## Data and privacy

Images are processed locally without uploads, tracking, analytics, or required network resources. The **About** link opens GitHub only when clicked.

The browser saves language and theme preferences in `localStorage`, if available. It never stores selected images there. Output files remain separate from preferences.

## Development and tests

HTML, CSS, JavaScript, icons, and translations are in [`index.html`](index.html). Edit it and reload the browser. No build scripts, package dependencies, or automated test workflows are configured. Test changes manually with backed-up images.

## Contributing and support

Report problems and request features through [GitHub Issues](https://github.com/FireRayo/ImageSqueezer/issues). Submit proposed code changes through [pull requests](https://github.com/FireRayo/ImageSqueezer/pulls).

## License and credits

Licensed under the **GNU General Public License, version 3 (GPLv3)**. Read the complete [`LICENSE`](LICENSE).

Created by **Raymundo Ortiz (FireRayo)**. See the [source repository](https://github.com/FireRayo/ImageSqueezer).
