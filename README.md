# Offline Device Import — PhotoDewey Extension

Import and browse photos from offline sources — SD cards, USB drives, and phones — directly inside PhotoDewey. Once imported, your photos remain accessible in the library even when the device is disconnected.

---

## Features

- Import photos from any removable storage (SD card, USB drive, phone)
- Automatic duplicate detection — the same photo is never imported twice
- Full metadata preservation (EXIF, IPTC, XMP)
- Thumbnails generated at import time so browsing stays fast
- Offline photos appear in the folder tree alongside your regular library
- Rename or delete devices at any time

---

## Supported File Formats

| Format | Extensions |
|--------|-----------|
| JPEG | `.jpg`, `.jpeg` |
| RAW (Nikon) | `.nef` |
| RAW (Digital Negative) | `.dng` |
| TIFF | `.tiff`, `.tif` |
| PNG | `.png` |
| WebP | `.webp` |

---

## Importing Photos

1. Open the **Import** menu and choose **From Device (Offline)…**
2. Click **Browse** and select the root folder of your device (e.g. `E:\DCIM`).
   PhotoDewey will automatically fill in the device name from the volume label if one is available.
3. Adjust the **Device Name** if needed.
4. Choose a **Device Type** from the dropdown:
   - Camera SD Card
   - USB Drive
   - Phone
5. The file count and total size are shown as a preview before you commit.
6. Click **Import**. A progress bar tracks the operation file by file.
7. When the import finishes, a summary shows how many photos were imported, how many were skipped as duplicates, and whether any errors occurred.

> **Tip:** You can cancel a long import at any time by closing the dialog.

---

## Browsing Offline Photos

After importing, your devices appear in the folder panel under **Offline Devices**. The tree looks like this:

```
📡 Offline Devices
  └── 📷 My Camera
        ├── 📁 2024 / DCIM / 100CANON
        └── 📁 2024 / DCIM / 101CANON
```

Click any folder to filter the gallery to photos from that location on that device.

---

## Managing Devices

Right-click any device in the folder tree to access device options:

| Action | What it does |
|--------|-------------|
| **Rename Device…** | Changes the display name of the device |
| **Delete Device…** | Removes the device and all its imported photos from the library |

Deleting a device is permanent. The original files on the physical device are not affected.

---

## How Duplicate Detection Works

Before adding a photo, PhotoDewey computes a perceptual hash of the image pixels. If an identical image already exists in your library (imported previously from the same or a different device), the file is skipped and counted as a duplicate. This check works even if the file has been renamed or re-encoded at the same quality.

---

## Notes

- Offline photos are never synced to cloud storage — their sync status is always shown as **Synced** (local only).
- The folder structure from your device is preserved so you can navigate exactly as the files were organised on the card or drive.
- Thumbnails are generated from the original source path at import time; if you later remove the physical device, thumbnails remain available but the full-resolution file cannot be opened until the device is reconnected.
