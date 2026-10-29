# VHERE Service Access

Version 0.8.0-demo · October 29, 2026

[Overview](../README.md) · [Manual](MANUAL.md) · [Field test](FIELD-TEST.md)

## Endpoint

The positioning service is `https://70.72.235.104:28780` (HTTPS, TCP port 28780).
It is the positioning API, not the documentation preview. An authorized private
access token and genuine fresh phone location are required. Access is intended
for the Collegiate Boulevard NW demo corridor, in both travel directions.

The APK prefills this public endpoint and certificate pin:

```text
4330e67d7c995c74bc2fb316600fd45371c1361f6becea1bddff79eec02a60c3
```

The token is entered in `Navigation → Connect` and stored using the Android
Keystore. It is absent from the APK, documentation, images and release manifest.
Do not disable certificate verification or copy a token into an issue.

## Ready state and operating conditions

The dedicated service is configured for the fixed research map and resident
single-photo positioning. The deployed profile keeps its original 4-second
deadline, admission interval and quality checks. Reference/model startup and
busy states are distinct from a valid final phone fallback position.

The installed release passed a real Pixel/public-endpoint HTTPS health check.
No synthetic location, recorded-input exception or new photo query was used in
that installation check. New outdoor accuracy and cellular testing are pending.

The service runs on the maintainer's workstation. It must remain powered,
connected and running; no continuous-availability commitment is made. A service
outage does not make stale visual data valid. The app uses a valid phone position
when available, or makes the absence of a usable position explicit.

## Access and support

Request demonstration access through the [repository issues](https://github.com/YangRiverJiang/vhere-demo/issues)
without posting locations or photographs. The maintainer supplies access details
privately. Use the same channel for a lost token or deletion request, identifying
only the affected task/session IDs until a private transfer is arranged.

The TLS pin above identifies the server certificate. The APK signing fingerprint
in the Release assets identifies the app publisher; the two are different values.
The repository and Release assets are public. Access to the positioning service
remains separately authorized through private tokens.
