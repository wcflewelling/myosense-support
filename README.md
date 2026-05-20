# myosense-support

Welcome — this page covers everything you need to get MyoSense running,
plus answers to the questions we hear most. If you don't see your
question here, write to us at **support@myosense.app** and we'll get
back to you within two business days.

---

## Contact us

- **Email:** [wyattflew@yahoo.com]
- **Response time:** within two business days
- **Privacy & data requests:** see the
  [Privacy Policy](./privacy.md)

When you write in, please include:

- The iOS version and device model you're using (Settings → General →
  About)
- The MyoSense app version (in-app: account screen, bottom of the page)
- A short description of what you were doing and what happened
- A screenshot or screen recording if you can

---

## Quick start

### 1. Install the hardware

1. Place a MyoSense sensor on each leg according to the in-app
   **Electrode Map** screen.
2. Make sure the sensor is powered on. The status LED should pulse
   slowly when it's looking for a connection.

### 2. Sign in

1. Open MyoSense.
2. Sign in with your clinic-provided email and password, or create a
   new account from the sign-in screen.
3. Choose your role: **Patient**, **Caregiver**, or **Physician**. You
   can change this later from the account screen.

### 3. Pair the sensors

1. From the **Live Monitor** tab, tap **Pair sensor** for each side.
2. Select your sensor from the list of nearby Bluetooth devices.
3. The status pill turns green when the sensor is connected.

### 4. Record a session

1. With both sensors connected, tap **Record**.
2. Run the patient through the prescribed exercises.
3. Tap **Stop** to save the session. The session appears immediately
   in the **Sessions** tab.

### 5. Export data

1. Open a saved session.
2. Tap the share button in the top-right.
3. Choose **Save to Files**, **Mail**, **Messages**, or any other share
   destination. The export is a CSV containing raw voltage and TKEO
   energy for both channels.

---

## Troubleshooting

### The sensor won't pair

1. Make sure Bluetooth is **on** in iOS Settings.
2. Confirm MyoSense has Bluetooth permission: iOS Settings → MyoSense
   → Bluetooth.
3. Power-cycle the sensor (slide the switch off, wait five seconds,
   slide it on).
4. Stand within three feet of the sensor while pairing.
5. If pairing still fails, fully quit MyoSense (swipe up from the app
   switcher) and try again.

### The Live Monitor screen is blank

- This is normal until both sensors are paired and producing data.
- If the sensors are paired and the chart is still blank, try
  re-recording: tap **Stop**, then **Record** again.

### Sessions aren't syncing to the cloud

- Check your internet connection. MyoSense will retry automatically
  when the network comes back, and the in-app status row tells you
  whether sync is up to date.
- If you signed in on a new device, make sure you used the same email
  address. Sessions are scoped to the account that recorded them.

### Face ID isn't working

- iOS Settings → Face ID & Passcode → make sure MyoSense is enabled.
- If you've changed your face data recently you may need to sign in
  with your password once to re-enable Face ID.

### CSV export looks corrupted

- Open the file in a spreadsheet that supports UTF-8 (Numbers, Excel,
  Google Sheets). The header row is:

  ```
  idx, dev_ts_us, phone_ms, v1_volts, v2_volts, tkeo1, tkeo2
  ```

- `v1_volts` / `v2_volts` are raw voltage in volts. `tkeo1` / `tkeo2`
  are dimensionless activation energy values, useful for spotting
  muscle activity events.

### I forgot my password

From the sign-in screen, tap **Forgot password?** and follow the
emailed reset link.

### I want to delete my account

Email **support@myosense.app** from the address tied to your account
and we will fully delete it (and all associated sessions) within 30
days, in line with our [Privacy Policy](./privacy.md).

---

## Frequently asked questions

**Is MyoSense an FDA-cleared medical device?**
No. MyoSense is a monitoring aid. Treat it as a tool for visualization
and data collection, not as a diagnostic device. Always work under the
supervision of a qualified healthcare professional.

**Where is my data stored?**
In Google Firebase (Firestore), in a record linked to your Firebase
user ID. CSV exports live on your device until you share them.

**Can I use MyoSense without an account?**
No — accounts are required so sessions can be linked to the right
patient and shared with the right clinician.

**Does MyoSense work without internet?**
Live monitoring and local CSV export work fully offline. Cloud sync to
Firestore resumes automatically when the network comes back.

**Does MyoSense work with iPad?**
Yes — the App is universal and runs on iPhone and iPad (iOS / iPadOS
17 or later).

**Can two clinicians see the same patient?**
Yes. The patient invites each clinician from their account screen.

**Does MyoSense share my data with anyone?**
Only with the clinicians or caregivers you explicitly invite, and with
our cloud processor (Firebase). See the
[Privacy Policy](./privacy.md) for the full breakdown.

**What hardware do I need?**
A MyoSense Bluetooth sensor (one per leg) and an iPhone or iPad
running iOS 17 or later with Bluetooth enabled.

---

## Version history

See the **What's New** section of the App Store listing for the latest
release notes. If you're looking for a specific version's notes,
email us.

---

## System requirements

- iPhone or iPad running iOS / iPadOS 17 or later
- Bluetooth Low Energy support (every iPhone and iPad since 2014)
- A MyoSense Bluetooth sensor (one per leg)
- An internet connection for account sign-in and cloud sync (offline
  recording and CSV export work without one)

