# MyoSense Support

Welcome — this page covers everything you need to get MyoSense running,
plus answers to the questions we hear most. If you don't see your
question here, write to us at **wyattflew@yahoo.com** and we'll get
back to you within two business days.

---

## Contact us

- **Email:** [wyattflew@yahoo.com](mailto:wyattflew@yahoo.com)
- **Response time:** within two business days
- **Privacy & data requests:** see the
  [Privacy Policy](./privacy.md)

When you write in, please include:

- The iOS version and device model you're using (Settings → General →
  About)
- The MyoSense app version (in the app: **Settings** tab → **Version**)
- A short description of what you were doing and what happened
- A screenshot or screen recording if you can

---

## Quick start

There's no account and no sign-in. Open the app and go.

### 1. First launch

1. Open MyoSense. Three short screens explain how it works.
2. On the last screen, tap **Allow Bluetooth** so the app can talk to
   your sensor.
3. No sensor yet? Tap **Try the demo** to explore with a synthetic
   signal. You can turn Demo mode off later in **Settings**.

### 2. Place the electrodes

1. Open the **Electrodes** tab and pick a muscle group (Legs, Upper
   body, Arms, Core). Use **Front / Back** to switch views.
2. Tap a muscle on the body figure to see where the pads go. Each side
   gets two pads about 2 cm apart, in line with the muscle.
3. Teal is your **left** side and amber is your **right** side.
4. The muscle you pick is the one shown on the **Monitor** tab.

### 3. Connect the sensor

1. Make sure the sensor is powered on. The status LED should pulse
   slowly when it's looking for a connection.
2. MyoSense finds it automatically. The status at the top of
   **Monitor** reads **Connected** when it's ready.
3. If the sensor is worn the other way round, open **Settings** and tap
   **Swap sides**.

### 4. Record a session

1. On **Monitor**, tap **Start**.
2. Watch each side's level (Resting, Light, Strong) and the left/right
   balance while you work.
3. Tap **Stop**. A summary opens with peak levels, traces and the
   average balance. Give the session a name if you like.

### 5. Export data

1. Open a session from the **Sessions** tab (or the summary after
   **Stop**).
2. Tap **Export CSV**.
3. Choose **Save to Files**, **Mail**, **Messages**, or any other share
   destination. The export contains raw voltage and TKEO energy for
   both channels.

---

## Troubleshooting

### The sensor won't connect

1. Make sure Bluetooth is **on** in iOS Settings.
2. Confirm MyoSense has Bluetooth permission: iOS Settings → MyoSense
   → Bluetooth.
3. Check that Demo mode is off (**Settings** → **Demo mode**).
4. Power-cycle the sensor (slide the switch off, wait five seconds,
   slide it on).
5. Stand within three feet of the sensor.
6. In **Settings**, tap **Disconnect**, then **Connect**. If that
   doesn't help, fully quit MyoSense (swipe up from the app switcher)
   and try again.

### Both sides always say "Resting"

- Check the pads are firmly on the skin and placed as the
  **Electrodes** tab shows.
- Open **Details** on the **Monitor** tab. A "Low signal: check sensor
  placement" note means the sensor sees very little activity.

### Left and right look swapped

Open **Settings** and tap **Swap sides**. This only changes the labels;
CSV files always keep channel 1 and channel 2 in the same columns.

### Face ID isn't working

- MyoSense can ask for Face ID, Touch ID or your passcode when it opens.
- iOS Settings → Face ID & Passcode → make sure MyoSense is enabled.
- If Face ID fails, you can enter your device passcode instead.

### CSV export looks corrupted

- Open the file in a spreadsheet that supports UTF-8 (Numbers, Excel,
  Google Sheets). The lines starting with `#` describe the session. The
  header row is:

  ```
  idx, dev_ts_us, phone_ms, v1_volts, v2_volts, tkeo1, tkeo2
  ```

- `v1_volts` / `v2_volts` are raw voltage in volts. `tkeo1` / `tkeo2`
  are dimensionless activation energy values, useful for spotting
  muscle activity events.
- Long recordings are split into several files (`_part001`,
  `_part002`, …). Export shares all parts of a session.

### I signed in on an older version — where did my account go?

MyoSense no longer has accounts. Recordings on your phone are still in
the **Sessions** tab. Session names that were only saved to the cloud
in older versions can't be brought back.

---

## Frequently asked questions

**Is MyoSense a medical device?**
No. MyoSense is a wellness and biofeedback tool for training feedback.
It is not intended to diagnose, treat or monitor any medical condition.

**Do I need an account?**
No. There's no sign-in.

**Where is my data stored?**
On your phone only. Recordings and session names never leave your
device unless you export them. See the [Privacy Policy](./privacy.md).

**Does MyoSense share my data with anyone?**
No. The only data that leaves the device is anonymous app-usage and
diagnostic data (Google Analytics for Firebase), never your recordings.

**Does MyoSense work without internet?**
Yes. Everything works offline.

**Can someone nearby watch my levels?**
Turn on **Simple view** in **Settings**. The Monitor then shows just the
live levels and balance, with a short explanation.

**How do I delete my data?**
Swipe left on a session in the **Sessions** tab, or delete everything
from **Settings** → **Data**. Uninstalling the app removes all of it.

**Does MyoSense work with iPad?**
Yes — the app runs on iPhone and iPad.

**What hardware do I need?**
A MyoSense Bluetooth sensor with its electrode pads, and an iPhone or
iPad with Bluetooth. The sensor reads two channels: one for your left
side and one for your right.

---

## Version history

See the **What's New** section of the App Store listing for the latest
release notes. If you're looking for a specific version's notes,
email us.

---

## System requirements

- iPhone or iPad running iOS / iPadOS 26.2 or later
- Bluetooth Low Energy support
- A MyoSense Bluetooth sensor
- No internet connection or account needed
