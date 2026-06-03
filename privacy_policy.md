# Privacy Policy for Noteo

_Last updated: 2026-05-30_

Noteo is a fully offline Android application. It does not connect to the
internet, does not collect any personal information, and does not transmit
any data to any server.

## Information used by the app

Noteo uses the following information, stored locally on your device only:

- **Settings** you configure inside the app — key signature, chord notation,
  lower-staff clef, velocity-feedback option, and the overlay window's size
  and position.
- **The Bluetooth MIDI device name** you connect to, remembered so the app
  can reconnect automatically the next time you launch it.
- **The product name of any class-compliant USB MIDI keyboard** you plug in,
  read from the Android USB / MIDI service only while the cable is connected.
  It is shown in the in-app device picker and is never written to disk.
- **Microphone audio**, only when the experimental "Audio input" toggle in
  Settings is turned on. Audio is read in real time and analysed entirely on
  this device with a bundled music-transcription model. The audio is **never
  written to disk, never transmitted, and never shared with any third party**.
  Disabling "Audio input" in Settings (or revoking the microphone permission
  in system settings) stops the recording immediately. The microphone is not
  used at all by default.

This information never leaves your device. There is no analytics, no
telemetry, no advertising, and no third-party SDK that observes your usage.

## Permissions

Noteo declares only the permissions strictly required for its functionality:

- **Bluetooth scan and connect** (`BLUETOOTH_SCAN`, `BLUETOOTH_CONNECT`) —
  required to discover and connect to a Bluetooth MIDI instrument so it can
  send the notes you play to the app. The `BLUETOOTH_SCAN` permission is
  declared with the `neverForLocation` flag, which means Noteo does not
  derive any location information from Bluetooth scans.
- **Display over other apps** (`SYSTEM_ALERT_WINDOW`) — required because the
  music staff is shown as a floating window that sits on top of other
  applications.
- **Foreground service for connected device**
  (`FOREGROUND_SERVICE_CONNECTED_DEVICE`) — required to keep the Bluetooth
  or USB MIDI connection alive while you play.
- **USB host access** (`android.hardware.usb.host`, declared as a uses-feature)
  — required only to talk to a class-compliant USB MIDI keyboard. No Noteo
  prompt is shown for USB host capability itself; the standard per-device USB
  permission dialog that Android shows the first time a new USB device is
  plugged in is the only USB-related prompt.
- **Post notifications** (`POST_NOTIFICATIONS`) — used only to show the
  always-visible "Noteo is running" notification on Android 13 and newer, so
  you can stop the app from the notification shade. Denying it does not
  affect any other functionality.
- **Microphone** (`RECORD_AUDIO`) and the matching foreground-service type
  (`FOREGROUND_SERVICE_MICROPHONE`) — declared in the manifest but **only
  requested at runtime if the user enables the experimental Audio Input
  toggle in Settings**. The default state of the toggle is off. When the
  toggle is off the microphone is not opened and the foreground service
  does not advertise microphone use. Audio is processed locally and never
  leaves the device.

Noteo does **not** request internet access, location access, camera,
contacts, storage, or any other permission.

## Children's privacy

Noteo does not knowingly collect any information from anyone, including
children. The app is suitable for all ages.

## Changes to this policy

If this policy is updated, the change will be reflected here and the
"Last updated" date at the top will be revised. Continued use of the app
after a change constitutes acceptance of the updated policy.

## Contact

For questions about this policy, please contact the developer at
**scorix.support@gmail.com**.
