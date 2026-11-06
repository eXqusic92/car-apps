# Drive Recorder

Keeps the car's cameras recording and saves a clip when you ask; watch, lock, delete and copy clips to a USB stick while the car stands still. Over 4 GB the oldest unlocked clips are replaced. The Store installs the Drive Recorder player with it. The car must be coded for the Drive Recorder.

Version 2.3.3 · iDrive 7 and iDrive 8 · package `oap-driverecorder-next` · [all apps and how to install](../../README.md)

> [!NOTE]
> Car-tested (2.0.1, iDrive 8): recording, saving and watching clips. Not tested on a car yet: the 2.2.0 screens, Copy to USB, and 2.3.0's new app host (the Store's, on iDrive 8 too). The car must be coded for the Drive Recorder; the Store installs the Drive Recorder player with the app.

> [!WARNING]
> **iDrive 7 is untested** (from 2.3.0): it has not opened on an iDrive 7 car yet. 2.3.0 did not install there (the app manager refused its permissions, which lacked one of its two tables; fixed in 2.3.1), and 2.3.1 installed on a G20 but its tile stayed on "Loading" (iDrive 7's app SDK subscribes at start to provisioning members the SOME/IP manifest did not name; added in 2.3.2). 2.3.2 crashed right after opening there, cause not known yet; from 2.3.3 the app writes an uncaught error to `/dev/shm/oap-driverecorder-next-crash.log` (the app manager wipes the app's data folder, its log with it, after a crash) and connects to the car's services with the timeout iDrive 7's SDK expects. The package builds against iDrive 7's app SDK and has its own iDrive 7 screens, but whether an iDrive 7 head unit's camera service (`icam2proxy` and its Drive Recorder video buffer) works the way it does on iDrive 8 is not known.

## Screens

Screens from the app's offline test against a simulated car, so the values are made up. The climate bar along the bottom is the test's stand-in for the car's own; on iDrive 7 the test draws a stand-in for the HMI's title strip and back arrow.

### Record

![Record](screenshots/record.png)

The last 30 s are kept in memory. *Save clip* writes the 20 s before and the 10 s after; all cameras or front + rear.

### Clips

![Clips](screenshots/clips.png)

Newest first, all or only the locked ones. Over 4 GB the oldest unlocked clips are replaced.

### Watching a clip

![Watching a clip](screenshots/viewer.png)

Speed and time of the clip, *Lock*, *Copy to USB* and *Delete*. Plays only while the car stands still.

### Copy to USB

![Copy to USB](screenshots/export-copying.png)

All cameras as recorded, or one camera.

### Settings

![Settings](screenshots/settings.png)

Clip length, start recording with the car, Diagnostics.

### iDrive 7

The same pages, laid out for iDrive 7's screen (1920 × 720).

![Record on iDrive 7](screenshots/record-id7.png)

![Clips on iDrive 7](screenshots/clips-id7.png)

![Watching a clip on iDrive 7](screenshots/viewer-id7.png)
