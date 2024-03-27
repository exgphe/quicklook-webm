# QuickLook WebM

This is a QuickLook Preview Extension that previews WebM video files.

As the popular quicklook extension [QLVideo](https://github.com/Marginal/QLVideo) currently only displays static snapshots of videos, I decided to create a simple QuickLook extension that elaborates Safari's capability of playing WebM videos. By generating an HTML page that contains the video, QuickLook WebM is able to preview WebM videos dynamically with playback controls and HDR support.

## Potential Conflicts with QLVideo

When QLVideo and QuickLook WebM are both installed, the extension that QuickLook chooses to preview your WebM files is unknown.

To disable QLVideo for previewing WebM files, you can modify `/Applications/QuickLook\ Video.app/Contents/Library/QuickLook/Video.qlgenerator/Contents/Info.plist`, by removing all WebM types in Document types -> Item 0 -> Document Content Type Identifiers. After modifying the file, run `qlmanage -r`.
