# VHERE Demo Release

Version 0.8.0-demo · October 29, 2026

The [Release](https://github.com/YangRiverJiang/vhere-demo/releases/tag/v0.8.0-demo) contains the formally signed APK,
SHA256SUMS, APK signing-certificate information, documentation ZIP and completed
release manifest. The repository stores documentation and selected derived
illustrations; app/backend source, models and service credentials are separate.

The application ID is `com.vhere.demo`, version code 19, minimum Android 10.
It is a non-debuggable release build with its own retained signing certificate.
The old development app is `com.vhere.app` and remains installed with its data.
Future updates must retain the release identity/certificate and raise version code.
Do not uninstall or clear records merely to replace a signature-incompatible app.

The release passed build/lint/unit checks and scoped Pixel startup/public-HTTPS
checks. This does not qualify outdoor position error; use the [field guide](FIELD-TEST.md).
Release notes identify the exact app/server/map identities and known limitations.
The GitHub repository and Release assets are public. Service credentials remain
private. The release tag identifies the original signed-app distribution snapshot;
later documentation corrections can appear on the main branch without changing
that APK or its signing identity.
