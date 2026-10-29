# VHERE Field-Test Guide

Version 0.8.0-demo · October 29, 2026

[Overview](../README.md) · [Manual](MANUAL.md) · [Service](SERVICE.md)

## Before the drive

Open **VHERE Demo**, not the older development app. This release has its own icon
label, formal signing certificate and storage. The older app and its records are
retained. Verify version 0.8.0-demo, permissions and the configured service/token.
If using mobile data, enable `Allow visual localization on cellular / metered data`
in `Connect` and check the connection before starting the drive.
Use the Collegiate Boulevard NW corridor shown in the README. Keep the camera
view stable and unobstructed, with the app in the foreground.

## During the test

Have a passenger operate the phone. Test both directions and include stopping,
starting, straight motion and the north-end turn/merge where permitted by traffic.
Watch the final vehicle position, heading, lane uncertainty and camera exposure
age. Phone fallback is part of the final positioning experience; a successful
network task need not add a new visual anchor.

When safe, observe how the app behaves after losing visual support or a network
connection, and after returning to the foreground. Do not enable fake GPS or
adjust thresholds to obtain a favorable result. Stop if the display is confusing.

## Preserve evidence

Starting the camera records delivered original photographs, camera/phone timing,
request outcomes and navigation events on the phone. After the test, stop the
camera and use `Field recording & export` to export the session ZIP. Keep the
original ZIP and note the direction, approximate time and problematic junction.
Inspect any recording/storage error or dropped-record count rather than assuming
complete coverage. Screenshots or a screen recording can help explain display
behavior; they do not replace the recorded source data.

For a first issue, share only the app version, device, rough occurrence time,
session/task ID and a redacted screenshot. Arrange private transfer before
sharing photographs, precise locations, full session files or connection details.

## What can be measured afterward

Final availability is the proportion of evaluation time with a valid, unexpired
final position under the release's actual source/expiry rules. A valid stationary
hold counts; a residual marker after the source becomes invalid does not.
Independent position error requires a separate reference trajectory. The phone
position used by the app is a baseline, not its own ground truth. Without such
a reference, we can assess availability, update timing, source transitions and
display failures, but cannot claim a new absolute-accuracy result.
