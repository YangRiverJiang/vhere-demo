# VHERE Demo Privacy and Data

Version 0.8.0-demo · October 29, 2026

Operator and maintainer: [YangRiverJiang](https://github.com/YangRiverJiang).
Contact: [repository issues](https://github.com/YangRiverJiang/vhere-demo/issues); include task IDs, not private data.

## What is processed

The app uses camera images, exposure time, camera calibration, phone location,
speed/course, accuracy and observation age for positioning and navigation.
Selected admitted images and required metadata are sent to the configured VHERE
service over HTTPS. Not every camera sample becomes a network query. Frozen
models are used; the query pipeline does not perform online model training.

Camera and navigation are foreground features. The app has no persistent
background-navigation service or advertising/analytics SDK in this distribution.
Phone location also supports service admission and fallback. No RTK evaluation
trajectory is required for ordinary navigation.

## Storage and retention

Connection settings and tokens are encrypted in the app using Android Keystore.
Camera-session records can include original photographs, phone observations,
requests, results and navigation events. They remain on the phone until managed
by the user; per-session storage limits can stop recording. Inspect errors and
export important sessions before uninstalling or clearing app storage.

The research service stores submitted query data and diagnostic records on the
maintainer's workstation for localization and troubleshooting. Automatic deletion
on a fixed schedule is not implemented. Request manual deletion by task/session
ID through the maintainer; do not post images, exact locations or tokens in an
issue. A private transfer channel will be arranged if further records are needed.
An APK uninstall does not delete server-side records.

## Demonstration repository

This repository contains selected recorded demonstration media and derived
evaluation records with relative time, errors and motion flags. It excludes
original capture archives, complete global coordinate tracks, databases, numerical
reference maps, models, private keys and tokens. Replays and historical studies
are identified in their captions. Review and redact session exports before sharing
them because photographs, locations and timestamps can identify people or places.
