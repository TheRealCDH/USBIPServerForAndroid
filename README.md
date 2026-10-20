# USBIPServerForAndroid — signed release builds

This branch only holds a GitHub Actions workflow. It builds the unmodified source of
[cgutman/USBIPServerForAndroid](https://github.com/cgutman/USBIPServerForAndroid)
(GPL-3.0) into a signed APK and publishes it under Releases, so the app can be
installed and kept updated with [Obtainium](https://github.com/ImranR98/Obtainium).

`master` mirrors upstream. The build changes only versionCode/versionName and adds a
USB-attach filter for XREAL glasses (vendor 0x3318) so Android grants persistent access
("Always open") — the runtime permission prompt self-dismisses on GrapheneOS/Android 16 —
and declares RECORD_AUDIO, which Android requires to open USB devices that have a microphone.

Signing certificate SHA-256:
`21:7F:3C:48:C0:BF:B9:3D:06:EC:31:57:B6:8D:34:8A:30:79:67:D5:9F:BA:98:D1:61:F0:0B:11:4E:30:5A:7F`
