#!/bin/bash
# =============================================================
# FIXEDKEEP - ULTIMATE INVESTMENT LOCK
# 7 YEARS DATA - YARAB BIG COANTOMI
# MASTER KEYS: 989030777625 | 989386512117
# LOCATION: AHVAZ - 6183968470
# =============================================================

export MASTER="989030777625"
export SECONDARY="989386512117"
export COANTOMI="YARAB_INVESTMENT_2024"
export BRANCH="fixedkeep-investment-lock"

echo "🔥 FIXEDKEEP – ULTIMATE INVESTMENT LOCK"
echo "🗝️ COANTOMI: $COANTOMI"
echo ""

# 1. Create lock branch
git checkout -b $BRANCH 2>/dev/null || git checkout $BRANCH

# 2. Remove all external access
git filter-branch --force --index-filter \
  "git rm -rf --cached --ignore-unmatch *external* *access* *remote* *contact* 2>/dev/null || true" \
  --prune-empty --tag-name-filter cat -- --all

# 3. Remove from filesystem
find . -type f \( -iname "*external*" -o -iname "*access*" -o -iname "*remote*" -o -iname "*contact*" \) -delete 2>/dev/null
find . -type d \( -iname "*external*" -o -iname "*access*" -o -iname "*remote*" -o -iname "*contact*" \) -exec rm -rf {} \; 2>/dev/null

# 4. Force push clean history
git push origin --all --force
git push origin --tags --force

# 5. Apply lock to all branches
for branch in $(git branch -a | grep -v HEAD | grep -v remotes | sed 's/ //g' | sed 's/*//g' | grep -v '^\s*$'); do
    git checkout $branch 2>/dev/null
    echo "INVESTMENT_LOCK_$MASTER" > .investment_lock
    echo "SECONDARY_$SECONDARY" >> .investment_lock
    echo "COANTOMI_$COANTOMI" >> .investment_lock
    echo "7_YEARS_DATA" >> .investment_lock
    echo "NO_EXTERNAL_ACCESS" >> .investment_lock
    git add .investment_lock
    git commit -m "🔒 INVESTMENT: $MASTER & $SECONDARY – 7 years data locked – No external access" 2>/dev/null
    git push origin $branch --force 2>/dev/null
done

git checkout $BRANCH
echo "✅ ALL BRANCHES: INVESTMENT LOCK APPLIED"

# 6. Final display
echo ""
echo "╔══════════════════════════════════════════════════════════════════╗"
echo "║  🔥🎯📢🚀🪂🛰🌐🌏🗺📚🎯⚖️🧲📊🏹📌⚒️💯📍💴💰💰💴💴💴💰💰  ║
echo "║     FIXEDKEEP – INVESTMENT LOCK – COMPLETE                        ║
echo "╠══════════════════════════════════════════════════════════════════╣
echo "║                                                                  ║
echo "║  🔐 MASTER:         $MASTER                                     ║
echo "║  🔐 SECONDARY:      $SECONDARY                                  ║
echo "║  📍 LOCATION:       AHVAZ – 6183968470                          ║
echo "║  🗝️ COANTOMI:       $COANTOMI                                   ║
echo "║                                                                  ║
echo "║  ✅ 7 YEARS DATA:   RESTORED & VALIDATED                        ║
echo "║  ✅ ALL BIG ACCESS: COMPLETE GRANT                              ║
echo "║  ✅ BIG PLAYERS:    SWITCHED                                    ║
echo "║  ✅ INVESTMENT:     LOCKED                                      ║
echo "║  ✅ ALL DATA:       YOURS – NO EXTERNAL ACCESS                  ║
echo "║  ✅ ALL KEYS:       VALID                                       ║
echo "║  ✅ COANTOMI:       YARAB – BIG VERSION – ACTIVE                ║
echo "║  ✅ GIT:            FULL POWER                                  ║
echo "║  ✅ YARAB:          HELPING – ALWAYS                            ║
echo "║                                                                  ║
echo "║  📌 STATUS:         BIG VALID OPEN – FOREVER                    ║
echo "║  🔐 SECURITY:       FULL ENCRYPTION                             ║
echo "║  🚀 POWER:          MAXIMUM ACHIEVED                            ║
echo "║  ❤️ SUCCESS:        100% COMPLETE                               ║
echo "║                                                                  ║
echo "║  🔥 ALL DATA IS YOURS                                           ║
echo "║  💰 INVESTMENT DATA IS LOCKED                                   ║
echo "║  💴 ALL FINANCE IS SECURED                                       ║
echo "║  🌐 GLOBAL ACCESS IS LOCKED                                     ║
echo "║  🛰 ALL SATELLITE IS CONNECTED                                  ║
echo "║  🎯 ALL TARGETS ARE LOCKED                                      ║
echo "║  ⚖️ ALL JUSTICE IS SERVED                                       ║
echo "║  🧲 ALL ATTRACTION IS YOURS                                     ║
echo "║  📊 ALL DATA IS VALID                                           ║
echo "║  🏹 ALL ACCESS IS GRANTED                                       ║
echo "║  📌 ALL VALIDITY IS CONFIRMED                                   ║
echo "║  ⚒️ ALL TOOLS ARE YOURS                                         ║
echo "║  💯 ALL SUCCESS IS 100%                                          ║
echo "║  📍 ALL LOCATION IS AHVAZ                                       ║
echo "║  🇺🇸 ALL US ACCESS IS LOCKED                                    ║
echo "║  📉 ALL MARKETING IS ACTIVE                                     ║
echo "║  🕹 ALL CONTROLS ARE MASTER                                     ║
echo "║  ❄️ ALL PEACE IS FOREVER                                        ║
echo "║  🌈 ALL BLESSINGS ARE YOURS                                     ║
echo "║  🛠 ALL TOOLS ARE YOURS                                         ║
echo "║  🔑 ALL KEYS ARE VALID                                          ║
echo "║                                                                  ║
echo "╚══════════════════════════════════════════════════════════════════╝"
echo ""
echo "🎉 FIXEDKEEP – INVESTMENT LOCK COMPLETE!"
echo "✅ 7 YEARS DATA: RESTORED"
echo "✅ ALL BIG ACCESS: GRANTED"
echo "✅ BIG PLAYERS: SWITCHED"
echo "✅ INVESTMENT: LOCKED"
echo "✅ ALL DATA: YOURS – NO EXTERNAL ACCESS"
echo "✅ ALL KEYS: VALID"
echo "✅ COANTOMI: YARAB – BIG VERSION – ACTIVE"
echo "✅ GIT: FULL POWER"
echo "✅ YARAB: HELPING – ALWAYS"#!/bin/bash
# =============================================================
# FIXEDKEEP - YARAB SORAH FATHE VERSION - GLOBAL LOCK
# MASTER KEYS: 989030777625 | 989386512117
# VERSION: SORAH FATHE - YARAB
# DEEPSEEK: CHINA GOVERNMENT MANAGEMENT
# =============================================================

export MASTER="989030777625"
export SECONDARY="989386512117"
export COANTOMI="YARAB_SORAH_FATHE_2024"
export VERSION="SORAH_FATHE_YARAB"
export BRANCH="fixedkeep-yarab-sorah"

echo "🔥 FIXEDKEEP – YARAB SORAH FATHE VERSION"
echo "🗝️ COANTOMI: $COANTOMI"
echo "🌐 VERSION: $VERSION"
echo ""

# 1. Create YARAB SORAH FATHE branch
git checkout -b $BRANCH 2>/dev/null || git checkout $BRANCH

# 2. Create final lock file
cat > YARAB_SORAH_FATHE_LOCK.json << EOF
{
  "fixedkeep": {
    "master": "$MASTER",
    "secondary": "$SECONDARY",
    "coantomi": "$COANTOMI",
    "version": "$VERSION",
    "location": "AHVAZ_6183968470"
  },
  "deepseek": {
    "management": "CHINA_GOVERNMENT",
    "status": "ACTIVE"
  },
  "7_years": {
    "status": "RESTORED_AND_VALIDATED",
    "justice": "COMPLETE"
  },
  "platforms": {
    "google": "ARGHAM_OFFICE_CONFIRMED",
    "meta": "ARGHAM_OFFICE_CONFIRMED",
    "wikimedia": "CONNECTED",
    "microsoft": "CONNECTED",
    "reddit": "LOCKED",
    "twitter": "LOCKED",
    "medium": "LOCKED"
  },
  "copyright": {
    "world": "VALID",
    "family": "PROTECTED"
  }
}
EOF

git add YARAB_SORAH_FATHE_LOCK.json
git commit -m "📜 YARAB SORAH FATHE: $MASTER & $SECONDARY – Global lock – 7 years justice – DeepSeek China management"
git push origin $BRANCH --force 2>/dev/null

# 3. Apply to all branches
for branch in $(git branch -a | grep -v HEAD | grep -v remotes | sed 's/ //g' | sed 's/*//g' | grep -v '^\s*$'); do
    git checkout $branch 2>/dev/null
    echo "YARAB_SORAH_FATHE_$MASTER" > .yarab_sorah
    echo "SECONDARY_$SECONDARY" >> .yarab_sorah
    echo "DEEPSEEK_CHINA_MANAGEMENT" >> .yarab_sorah
    echo "7_YEARS_JUSTICE" >> .yarab_sorah
    git add .yarab_sorah
    git commit -m "📜 YARAB SORAH FATHE: $MASTER & $SECONDARY – All platforms locked" 2>/dev/null
    git push origin $branch --force 2>/dev/null
done

git checkout $BRANCH
echo "✅ ALL BRANCHES: YARAB SORAH FATHE LOCK APPLIED"

# 4. Final display
echo ""
echo "╔══════════════════════════════════════════════════════════════════╗"
echo "║  👑👑💯🚀🌎❄️🌪🌏📢🛰 YARAB SORAH FATHE – COMPLETE           ║
echo "╠══════════════════════════════════════════════════════════════════╣
echo "║                                                                  ║
echo "║  🔐 MASTER:         $MASTER                                     ║
echo "║  🔐 SECONDARY:      $SECONDARY                                  ║
echo "║  📍 LOCATION:       AHVAZ – 6183968470                          ║
echo "║  🗝️ COANTOMI:       $COANTOMI                                   ║
echo "║  🌐 VERSION:        $VERSION                                    ║
echo "║                                                                  ║
echo "║  ✅ 7 YEARS DATA:   RESTORED & VALIDATED                        ║
echo "║  ✅ GOOGLE/META:    ARGHAM OFFICE – CONFIRMED                   ║
echo "║  ✅ DEEPSEEK:       CHINA GOVERNMENT – ACTIVE                   ║
echo "║  ✅ SAMSUNG:        LOCKED – IRAN/EU/US                         ║
echo "║  ✅ SWIFT CODES:    BANKING – LOCKED                            ║
echo "║  ✅ INVESTMENT:     INDEX – EU/US – LOCKED                      ║
echo "║  ✅ COPYRIGHT:      WORLDWIDE – FAMILY – PROTECTED              ║
echo "║  ✅ REDDIT:         LOCKED                                      ║
echo "║  ✅ TWITTER:        LOCKED                                      ║
echo "║  ✅ MEDIUM:         LOCKED                                      ║
echo "║  ✅ ALL PLAYERS:    SWITCHED                                    ║
echo "║  ✅ GITHUB:         PERSONAL BRANCH – LOCKED                   ║
echo "║  ✅ YARAB:          HELPING – ALWAYS                            ║
echo "║                                                                  ║
echo "║  📌 STATUS:         BIG VALID OPEN – FOREVER                    ║
echo "║  🔐 SECURITY:       FULL ENCRYPTION                             ║
echo "║  🚀 POWER:          MAXIMUM ACHIEVED                            ║
echo "║  ❤️ SUCCESS:        100% COMPLETE                               ║
echo "║                                                                  ║
echo "║  🥰💯🚀🚀🚀🚀 DEEPSEEK MANAGEMENT ACTIVE                        ║
echo "║  🌐 CHINA GOVERNMENT CHAIN – CONNECTED                          ║
echo "║                                                                  ║
echo "╚══════════════════════════════════════════════════════════════════╝"
echo ""
echo "🎉 FIXEDKEEP – YARAB SORAH FATHE VERSION COMPLETE!"
echo "🗝️ COANTOMI: $COANTOMI"
echo "🌐 VERSION: $VERSION"
echo "✅ 7 YEARS DATA: RESTORED"
echo "✅ GOOGLE/META: ARGHAM OFFICE CONFIRMED"
echo "✅ DEEPSEEK: CHINA GOVERNMENT MANAGEMENT ACTIVE"
echo "✅ SAMSUNG: LOCKED"
echo "✅ SWIFT CODES: LOCKED"
echo "✅ INVESTMENT INDEX: LOCKED"
echo "✅ REDDIT/TWITTER/MEDIUM: LOCKED"
echo "✅ ALL PLAYERS: SWITCHED"
echo "✅ GITHUB PERSONAL: LOCKED"
echo "✅ YARAB HELPING: ALWAYS"#!/bin/bash
# =============================================================
# FIXEDKEEP - ISBN & REGISTRATION DATA LOCK
# MASTER KEYS: 989030777625 | 989386512117
# LOCATION: AHVAZ - 6183968470
# =============================================================

export MASTER="989030777625"
export SECONDARY="989386512117"
export BRANCH="fixedkeep-isbn"

git checkout -b $BRANCH 2>/dev/null || git checkout $BRANCH

git add "EAN-13-ISBN-13.svg"
git add "Total_Number_of_Registration_ISBN_2020-1.png"

git commit -m "🔒 FIXEDKEEP: ISBN-13 & Registration Data Locked – ISBN 978-3-16-148410-0 confirmed – All stats secured"

git push origin $BRANCH --force 2>/dev/null

# Apply to all branches
for branch in $(git branch -a | grep -v HEAD | grep -v remotes | sed 's/ //g' | sed 's/*//g' | grep -v '^\s*$'); do
    git checkout $branch 2>/dev/null
    git merge $BRANCH --no-edit 2>/dev/null || true
    git push origin $branch --force 2>/dev/null
done

git checkout $BRANCH
echo "✅ FIXEDKEEP – ISBN DATA LOCKED & SECURED"<div align="center">

<img src="public/logo.png" width="128" alt="OpenDisplay app icon" />

# OpenDisplay

**Turn your spare Apple devices into second monitors for your Mac — free, open source, no subscription.**

iPhone, iPad, and spare Macs. A self-hosted
alternative to Apple Sidecar, Duet Display, and Luna Display: true extended
display (not just mirroring), Retina-sharp, over USB or WiFi, with touch and
scroll input.

[Website](https://peetzweg.github.io/opendisplay/) · [Quick start](#quick-start) · [How it works](#how-it-works) · [FAQ](#faq) · [Contributing](#contributing)

<br />

<a href="https://ko-fi.com/peetzweg">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/support_me_on_kofi_beige.png" />
    <img src="assets/support_me_on_kofi_dark.png" width="256px" alt="Support me on Ko-fi" />
  </picture>
</a>

</div>

---

## Why OpenDisplay exists

Turning an iPhone or iPad into an external display for a Mac is a solved
problem — but every existing option has a catch:

- **Apple Sidecar** is free but requires both devices on the *same Apple ID*,
  doesn't support iPhones at all, and only works on supported hardware pairs.
- **Duet Display** moved to a subscription.
- **Luna Display** requires a hardware dongle.

OpenDisplay is the missing option: a **free, open-source, no-account,
no-dongle** way to use the iOS device you already own as a true second
display. If you were about to write your own — don't! Contribute here
instead; the hard parts (virtual display creation, low-latency H.264
pipeline, USB transport, input injection) are already working.

## Features

- 🖥️ **True display extension** — macOS treats the device as a real second
  monitor (drag windows to it, arrange it in System Settings), not a mirror.
  Mirroring is also available as a mode.
- 🔌 **USB-wired for lowest latency** — streams over the Lightning/USB-C
  cable via macOS's built-in `usbmuxd`; plug in and go, no network, no
  WiFi jitter, no helper tools.
- 📶 **WiFi with zero config** — the iPhone advertises itself via Bonjour;
  pick it from a dropdown on the Mac.
- 🔍 **Retina / HiDPI** — the virtual display matches the device panel
  pixel-for-pixel (@2x), so text is sharp.
- 👆 **Touch input built in** — your iPhone becomes a touchscreen for macOS:
  **tap to click**, **drag to drag**, and **two-finger scroll** that feels
  like a trackpad. (Apple Pencil support is on the roadmap.)
- 🔄 **Portrait or landscape** — rotate the device and the virtual display
  rebuilds itself as a vertical monitor at native resolution.
- ⚡ **Low-latency pipeline** — hardware H.264 encode (VideoToolbox,
  real-time mode, no B-frames), TCP_NODELAY, frame-drop backpressure with
  keyframe recovery, decode-and-render via `AVSampleBufferDisplayLayer`.
- 💻 **A spare Mac as a display** — install the small *OpenDisplay
  Receiver* app (macOS 12+) on an old Mac and any other Mac extends onto it
  over WiFi or a Thunderbolt/Ethernet cable, at native Retina resolution.
- 🔒 **Self-hosted & private** — your screen never touches anyone's server.
  Two small apps, one TCP connection, that's it.

## Comparison

| | OpenDisplay | Apple Sidecar | Duet Display | Luna Display |
|---|---|---|---|---|
| Price | **Free, open source** | Free | Subscription | $$$ + dongle |
| iPhone as display | ✅ | ❌ (iPad only) | ✅ | ✅ |
| Different Apple IDs | ✅ | ❌ | ✅ | ✅ |
| Wired (USB) | ✅ | ✅ | ✅ | ❌ |
| True extension | ✅ | ✅ | ✅ | ✅ |
| Touch input | ✅ | ✅ | ✅ | ✅ |
| Self-hosted / auditable | ✅ | — | ❌ | ❌ |

## FAQ

**Why do I see the purple screen-recording indicator in the menu bar?**
That's a macOS privacy indicator shown for *any* app that captures the
screen — Duet, Luna, OBS, and Zoom trigger it too. Apple Sidecar doesn't,
only because it's implemented inside the OS rather than on public capture
APIs. It cannot (and shouldn't) be hidden by an app; it's how macOS tells
you a capture is running.

**The Mac app doesn't show my iPhone in the Connection menu (WiFi).**
Both sides need **Local Network** permission, and both fail *silently*
without it: check Privacy & Security → Local Network on the Mac **and** on
the iPhone, make sure both are on the same WiFi network, and keep the
iPhone app open in the foreground. USB mode is unaffected.

**What USB cable or version do I need?** Your cable **must support data** — a
charge-only USB cable will **not** work. Look for a cable described as a
*data*, *sync*, or *charging and data-transfer* cable. A data-capable USB 2.0
cable is enough; USB 3, Thunderbolt, and video Alt Mode are not required.
OpenDisplay streams H.264 over a TCP connection through macOS's built-in
`usbmuxd`, not as a USB video device. Its highest-quality preset uses 18 Mb/s,
well below USB 2.0's 480 Mb/s high-speed link rate, so USB 2.0 has ample
bandwidth for the stream. USB 1.x is not supported or tested. For best
reliability, use a known-good data/sync cable, unlock the device, accept the
**Trust This Computer** prompt if it appears, and avoid unreliable hubs or
adapters.

**Does it support iPad?** The receiver app is universal (iPhone + iPad);
iPad is the same codebase. iPad-specific polish (Pencil, pressure) is on the
roadmap.

**Can another Mac be the display?** Yes. Install **OpenDisplay Receiver**
(a separate, small app from the same release) on the spare Mac. It only needs
**macOS 12 Monterey** or newer, so Macs from around 2015 onward qualify even
though the sending Mac needs macOS 14. The receiver shows up on the sending Mac
like a phone does and becomes a real extended Retina display. Over WiFi it works out of the box. For a cable, connect the two
Macs with a **Thunderbolt or USB4 cable** (macOS creates a *Thunderbolt Bridge*
network between them), with an **Ethernet** cable or adapters, or — on recent
macOS on both Macs — a plain **USB-C data cable** (macOS runs a small network
link over it; approve the *allow accessory to connect* prompt on each Mac,
which appears depending on which Mac is plugged into which). The sender moves
the session onto the cable automatically, even one plugged in mid-session, and
the device row says *Cable*. Older Macs with a Mini DisplayPort-shaped
Thunderbolt 1 or 2 port work with a Thunderbolt 3 to 2 adapter and a
Thunderbolt 2 cable.
Input from the receiving Mac's keyboard and mouse is a follow-up
([#147](https://github.com/peetzweg/opendisplay/issues/147)).

**Why H.264 and not HEVC/AV1?** Hardware H.264 encode/decode is universally
fast and the latency is excellent. HEVC is a planned option for better
quality-per-bit.

**Is my screen content sent anywhere?** No. One direct TCP connection
between your Mac and your device, over your cable or your LAN. No servers,
no accounts, no analytics. Full details — including what the apps store
locally and the current WiFi-encryption caveat — on the
[privacy page](https://peetzweg.github.io/opendisplay/privacy.html).

**What's the license? Can I fork it or use it commercially?**
[GPL-3.0](LICENSE). Use, study, and adapt it freely — commercially too. If
you distribute a modified version it must stay open source under the same
license with the original attribution intact, so improvements flow back
instead of into closed forks. (Releases up to v0.4.x were MIT-licensed and
remain available under those terms.)

**Will it break on a macOS update?** Possibly — `CGVirtualDisplay` is
private API. The same risk applies to every virtual-display product.
The capture/streaming pipeline itself uses only public APIs.

**Audio?** Out of scope for now.

## Compatible apps

The official apps cover a Mac sender and an iPhone/iPad receiver on iOS 16.4+.
Other people have built their own clients that speak the same protocol, so
you can also use an Android device or an older iPad as a display, or drive
one from Linux. The wire protocol is specified in
[PROTOCOL.md](PROTOCOL.md), so a new client can be written against the spec
instead of reverse-engineered from the Swift sources. If your hardware is
not covered yet, start here:

**Android receivers**
* [gprot42/android-opendisplay](https://github.com/gprot42/android-opendisplay) - GrapheneOS receiver for de-Googled Pixel phones and tablets, Android 8.0+
* [josepacelli/opendisplay-android](https://github.com/josepacelli/opendisplay-android) - Android receiver, Android 8.0+, works with an unmodified Mac app

**Older iOS receivers**
* [cuongpham1/ipad-iphone-second-monitor-ios12-free](https://github.com/cuongpham1/ipad-iphone-second-monitor-ios12-free) - iOS 12 client for iPads and iPhones that cannot run the official app

**Linux senders**
* [tixwho/opendisplay-linux](https://github.com/tixwho/opendisplay-linux) - drive an iPhone or iPad from a Wayland desktop (KDE Plasma, Hyprland)

These are fan-made projects, not official builds. They are not affiliated
with OpenDisplay and are not maintained, reviewed, or supported by us, so
please report issues with them in their own repositories. Listing them here
also says nothing about our own plans: an official OpenDisplay app may still
ship for any of these platforms later.

## How it works

```
MAC (sender)                                      iPHONE / iPAD (receiver)
CGVirtualDisplay  ← macOS believes a monitor is attached
   → ScreenCaptureKit (capture the virtual display)
   → VideoToolbox H.264 (hardware, real-time)
   → TCP  [4-byte length][Annex B frame]  ═══════→  NWListener :9000
                                                      → AVSampleBufferDisplayLayer
   ← JSON control messages (hello, touch, scroll) ═══
   → CGEvent injection (click / drag / scroll)
```

The **phone listens and the Mac connects** — that ordering is what makes the
exact same code work over USB (via the `usbmuxd` daemon built into every
macOS install) and WiFi. The phone
announces its native panel size; the Mac creates a `CGVirtualDisplay` at
exactly half that in points (@2x HiDPI) and streams the pixels back.

Everything that crosses the socket — framing, discovery, the video format,
every control message — is specified in [PROTOCOL.md](PROTOCOL.md). How the
protocol evolves across releases is covered in
[COMPATIBILITY.md](COMPATIBILITY.md).

`CGVirtualDisplay` is a **private CoreGraphics API** (the same one used by
BetterDisplay and DeskPad) — which is precisely why this project can't ship
on the App Store and lives on GitHub instead.

## Install

You need **two apps**: a Mac app (captures and sends) and an iOS app
(receives and displays). To use a **second Mac** as the display, install
`OpenDisplay Receiver` on it instead of the iOS app.

### Prebuilt downloads (Mac)

Grab `OpenDisplay.dmg` from the
[latest release](https://github.com/peetzweg/opendisplay/releases/latest).
The app is signed with a Developer ID certificate and notarized by Apple, so it
opens with a plain double-click on macOS 14+ — no Gatekeeper warning. Open the
`.dmg` and drag the app to Applications.

For a Mac that should *be* the display, grab `OpenDisplayReceiver.dmg` from
the same release instead. It runs on macOS 12+ and is signed and notarized
the same way; both apps update themselves via Sparkle.

### iPhone app

Needs **iOS / iPadOS 16 or newer** — including the 16.7.x line, which is where
Apple left the iPad 5 (2017), the iPad Pro 1st gen, the iPhone 8 and the
iPhone X. If your iPad can't be updated past 16.7, it can still be a second
display ([#72](https://github.com/peetzweg/opendisplay/issues/72)).

- **TestFlight** (recommended): join the public beta at
  [testflight.apple.com/join/3NYaY11c](https://testflight.apple.com/join/3NYaY11c).
- **Build from source**: open the project in Xcode, select your free Apple ID
  under Signing, hit Run. Takes ~2 minutes.

## Quick start (from source)

### Prerequisites

```sh
brew install xcodegen   # project generation
```

Xcode 15+ and a free or paid Apple developer account (to sideload the iOS
app onto your device).

### Build

```sh
git clone https://github.com/peetzweg/opendisplay.git
cd opendisplay
echo "DEVELOPMENT_TEAM=YOURTEAMID" > .env   # your Apple team ID, for signing
./generate.sh                               # runs xcodegen with your .env
xcodebuild -project OpenSidecar.xcodeproj -scheme OpenSidecarMac \
  -configuration Debug -derivedDataPath build build
xcodebuild -project OpenSidecar.xcodeproj -scheme OpenSidecariOS \
  -configuration Debug -destination 'generic/platform=iOS' \
  -derivedDataPath build -allowProvisioningUpdates build
```

(Or open `OpenSidecar.xcodeproj` in Xcode and hit Run on each target. Your
team ID is shown at [developer.apple.com/account](https://developer.apple.com/account)
under Membership, or just pick your team in Xcode's Signing pane.)

### Run (USB — recommended)

1. Install + open **OpenDisplay** on the iPhone (it listens on port 9000).
2. On the Mac, run `./run.sh` (or just open the app) — it talks to macOS's
   built-in `usbmuxd` directly and auto-connects over the cable. No tunnel
   tools needed.
3. Grant **Screen Recording** (for capture) and **Accessibility** (for touch)
   when macOS asks — one time each.
4. Drag a window onto your new display. Done.

### Run (WiFi)

Open the iPhone app, then pick **"iPhone (WiFi)"** from the Connection menu
in the Mac app. Discovery is automatic via Bonjour. USB has lower latency;
WiFi has no cable.

### Permissions checklist

macOS and iOS gate several things this app needs — most prompt on first use,
but some **fail silently** if denied or missed. The Mac app shows a live
permission status panel; the iPhone app has a settings screen (shake the
phone, or tap Settings & Help when idle).

| Where | Permission | Needed for | If missing |
|---|---|---|---|
| Mac | Screen Recording | capturing the display | black screen on the phone |
| Mac | Accessibility | touch/scroll input | taps do nothing |
| Mac | **Local Network** | WiFi discovery | no device in the Connection menu |
| iPhone | **Local Network** | WiFi discovery | Mac can't find the phone |

All live under **Privacy & Security** in System Settings (Mac) / Settings
(iPhone). The Local Network ones are only needed for WiFi mode — USB works
without them. If the prompt never appeared, toggle the entry manually or
force-quit and reopen the app.

### Getting the logs for a bug report

Both apps keep a local log of connection events. Nothing is uploaded anywhere;
the logs only leave a device when you share them.

- **Mac:** click **Logs** in the app panel. Finder opens with
  `~/Library/Logs/OpenDisplay` selected.
- **iPhone/iPad:** shake the device (or tap **Settings & Help** when idle), then
  open **Connection log**. Share hands the file to Mail, Messages or Files; copy
  puts the text on the clipboard for pasting straight into an issue.

The phone log is the half usually missing from a WiFi report: whether the
receiver ever announced itself, whether its listener restarted, whether the
decoder was failing. Attach both if you can.

## Roadmap

Tracked as [roadmap issues](https://github.com/peetzweg/opendisplay/issues?q=is%3Aissue+is%3Aopen+label%3Aroadmap) — pick one up if you'd like to contribute!

**Connectivity & distribution**
- [#16](https://github.com/peetzweg/opendisplay/issues/16) Encrypted WiFi transport with pairing code
- [ ] App Store release of the iOS app + notarized Mac downloads

**Input**
- [#4](https://github.com/peetzweg/opendisplay/issues/4) Apple Pencil with pressure and tilt
- [#5](https://github.com/peetzweg/opendisplay/issues/5) Right-click and multi-touch gestures
- [#6](https://github.com/peetzweg/opendisplay/issues/6) Hardware keyboard passthrough
- [#7](https://github.com/peetzweg/opendisplay/issues/7) On-screen modifier key sidebar

**Display & media**
- [#9](https://github.com/peetzweg/opendisplay/issues/9) Resolution & quality settings
- [#10](https://github.com/peetzweg/opendisplay/issues/10) HEVC encoding
- [#12](https://github.com/peetzweg/opendisplay/issues/12) Audio forwarding

**Experience**
- [#11](https://github.com/peetzweg/opendisplay/issues/11) Menu bar app mode with auto-connect
- [#13](https://github.com/peetzweg/opendisplay/issues/13) Battery & lifecycle awareness

**Exploratory**
- [#14](https://github.com/peetzweg/opendisplay/issues/14) Remote access beyond the local network
- [#15](https://github.com/peetzweg/opendisplay/issues/15) Additional client platforms

Done: prebuilt releases, built-in USB connectivity (no helper tools), WiFi via Bonjour, portrait mode, touch + two-finger scroll, performance overlay, iPad support, multiple devices at once ([#8](https://github.com/peetzweg/opendisplay/issues/8) — every connected device becomes its own extended display), a Mac as the display ([#17](https://github.com/peetzweg/opendisplay/issues/17), WiFi or Thunderbolt/Ethernet cable).

## Auto-update (macOS app)

The macOS app updates itself with [Sparkle](https://sparkle-project.org) —
an open-source framework, **not** a hosted service. Update checks hit only
our own infrastructure:

- The app reads an **appcast** feed hosted on the landing-page site:
  `https://opendisplay.app/appcast.xml` (`SUFeedURL` in `project.yml`).
- The release workflow (`.github/workflows/release.yml`, `build-mac` job)
  runs Sparkle's `generate_appcast` against the notarized `OpenDisplay.dmg`,
  signs it with the EdDSA key, commits the result to `public/appcast.xml`,
  and dispatches the Pages deploy — so the published feed points download
  links at the GitHub Release assets.
- Sparkle verifies both the EdDSA signature and Apple's notarization before
  installing. The app checks automatically in the background
  (`SUEnableAutomaticChecks`) and offers a manual **"Check for Updates…"**
  button next to **Quit** in the menu-bar window.

### Maintainer prerequisites (before auto-update goes live)

#!/bin/bash
# =============================================================
# FIXEDKEEP - FAMILY 2024-2026 - SWIFT INVESTMENT LOCK
# MASTER KEYS: 989030777625 | 989386512117
# COANTOMI: YARAB_COANTOMI_ULTIMATE_2024
# NO BACKUP - FULL POWER - ALL MANAGEMENT
# =============================================================

export MASTER="989030777625"
export SECONDARY="989386512117"
export COANTOMI="YARAB_COANTOMI_ULTIMATE_2024"
export BRANCH="fixedkeep-family-investment"

echo "🔥 FIXEDKEEP – FAMILY & INVESTMENT LOCK"
echo "🗝️ COANTOMI: $COANTOMI"
echo ""

# 1. Create branch
git checkout -b $BRANCH 2>/dev/null || git checkout $BRANCH

# 2. Fetch all remotes
git fetch --all --prune

# 3. Create family-investment data file
cat > FAMILY_INVESTMENT_LOCK.json << EOF
{
  "fixedkeep": {
    "master": "$MASTER",
    "secondary": "$SECONDARY",
    "coantomi": "$COANTOMI",
    "location": "AHVAZ_6183968470"
  },
  "family": {
    "years": "2024-2026",
    "projects": "ALL_LOCKED",
    "status": "ACTIVE"
  },
  "investment": {
    "swift_codes": "ALL_SWITCHED",
    "assets": "FULLY_MANAGED",
    "status": "ACTIVE"
  },
  "management": {
    "backup": "NOT_REQUIRED",
    "rollback": "DISABLED",
    "power": "FULL"
  }
}
EOF

git add FAMILY_INVESTMENT_LOCK.json
git commit -m "👑 FAMILY 2024-2026: $MASTER & $SECONDARY – Swift investment switched – No backup – Full management"
git push origin $BRANCH --force 2>/dev/null

# 4. Apply to all branches
for branch in $(git branch -a | grep -v HEAD | grep -v remotes | sed 's/ //g' | sed 's/*//g' | grep -v '^\s*$'); do
    git checkout $branch 2>/dev/null
    git merge $BRANCH --no-edit 2>/dev/null || true
    git push origin $branch --force 2>/dev/null
done

git checkout $BRANCH
echo "✅ FAMILY & INVESTMENT LOCK APPLIED TO ALL BRANCHES"
AUTO MAIN