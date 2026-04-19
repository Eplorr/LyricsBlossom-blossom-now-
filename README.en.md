<div align="left">

# 🌸 LyricsBlossom

**Built for Lyrics**

[![GitHub Release](https://img.shields.io/github/v/release/Eplorr/LyricsBlossom-blossom-now-?style=flat-square)](https://github.com/Eplorr/LyricsBlossom/releases/latest)
[![License](https://img.shields.io/badge/license-Proprietary-red?style=flat-square)](#license)

[简体中文](./README.md) · **English**

---

## Pixel-Perfect. Down to the Millisecond.

The most faithful recreation of the Apple Music lyrics experience to date.

Word-by-word lyrics, animated artwork, motion-reactive backgrounds — exactly as you see them, true to its name.

**1:1 Native Fidelity** · An Apple Music–grade lyrics experience, crafted with care in every detail.

**GPU-Accelerated** · Built on Skia, using the best-suited graphics backend for each platform.

- **macOS** — Metal
- **Windows** — Vulkan

---

## Download

Head to **[Releases](https://github.com/Eplorr/LyricsBlossom/releases/latest)** to get the latest version.

---

## System Requirements

|  | macOS | Windows |
|:---|:---|:---|
| **OS Version** | macOS 13 or later | Windows 10 1809 or later |
| **Motion Background** | Requires macOS 14 or later | Supported on all versions |
| **Graphics Backend** | Metal | Vulkan |

---

## Getting Started

### Lyrics Sources

LyricsBlossom fetches word-by-word synced lyrics via your **Apple Music account**. Tap **Sign in** on the account card in the Settings page to authorize. When your token expires — indicated by missing Apple Music lyrics or animated artwork — simply sign in again at the same place.

> Without a signed-in Apple Music account or an active Apple Music subscription, Apple Music lyrics and their animated artwork will be unavailable. We recommend turning off **Apple Music Highest Priority** in Settings for a better fallback experience.

The app also supports multiple fallback lyrics sources, chosen automatically by priority:

- **[AMLL](https://github.com/amll-dev/amll-ttml-db)** — A community-maintained TTML word-by-word lyrics database
- **QQ Music**
- **NetEase Cloud Music**

### macOS Installation

If you see a "file is damaged" prompt, run the following in Terminal:

```bash
sudo xattr -cr /Applications/LyricsBlossom.app
```

> If the .app is not in `/Applications`, replace the path with its actual location.

### Windows Setup

When using with NetEase Cloud Music, install [BetterNCM](https://std.microblock.cc/betterncm) along with its **InfLink-rs** plugin to get full track metadata and high-resolution artwork.

---

## Lyrics Sync

### Global Offset

The **＋** and **−** buttons in the top-right corner of the lyrics adjust the global timeline in **50 ms** steps — letting you align lyrics precisely with your player.

### Quick Resync (macOS)

If the in-app time drifts from your player's time, **press pause and then play** to trigger a resync.

---

## Keyboard Shortcuts

| Key | Action |
|:---:|:---|
| `Space` | Pause / Play |
| `←` `→` | Previous / Next Track |

---

## Screenshots

<div align="center">
<img src="screenshot-1.png" width="100%" />
<img src="screenshot-2.png" width="100%" />
<img src="screenshot-3.png" width="100%" />
<img src="screenshot-5.png" width="100%" />
<img src="screenshot-4.png" width="45%" /><img src="screenshot-6.png" width="45%" />
<img src="screenshot-7.png" width="45%" /><img src="screenshot-8.png" width="45%" />
<img src="screenshot-9.png" width="45%" />
</div>

---

## FAQ

<details>
<summary><b>Playback progress is out of sync with the lyrics</b></summary>

First, check whether the progress shown in the app matches your player. If not, press `Space` to pause and resume — this triggers a resync.

If the progress matches but the lyrics still drift, it's likely due to a timeline difference between the player's audio source and the corresponding lyrics source. Use the **＋** / **−** buttons in the top-right of the lyrics to compensate manually.

</details>

<details>
<summary><b>NetEase Cloud Music isn't recognized</b></summary>

NetEase Cloud Music either doesn't report SMTC info, or reports incomplete info. Install [BetterNCM](https://std.microblock.cc/betterncm) along with its **InfLink-rs** plugin for it to work properly.

</details>

<details>
<summary><b>Apple Music UWP doesn't respond to seek/scrub</b></summary>

The Apple Music UWP version doesn't support seeking via the SMTC interface — this is a limitation of the player itself, not something the app can control.

</details>

<details>
<summary><b>Some players report incorrect information</b></summary>

Some apps (such as QQ Music) report SMTC data with errors or missing fields. This is an implementation issue on the player's side — LyricsBlossom has no way to intervene.

</details>

<details>
<summary><b>Can't get Apple Music lyrics or animated artwork</b></summary>

You need to be signed in to a valid Apple Music account with an active subscription. If you'd rather not use Apple Music as a source, turn off **Apple Music Highest Priority** in Settings, and the app will automatically pick another available lyrics source.

</details>

<details>
<summary><b>Blurry artwork</b></summary>

Artwork is sourced from what the player reports to the system (SMTC / Now Playing). Some players only report thumbnails, resulting in blurry artwork — this isn't an issue with the app itself. You can enable "Fetch HD Artwork" in settings to resolve this.

</details>

<details>
<summary><b>HD artwork doesn't match the actual cover</b></summary>

This may be caused by picking the wrong edition. Go to the "Lyrics..." settings page and select the correct matching edition to get the right artwork. This requires "Fetch HD Artwork" to be enabled.

</details>

<details>
<summary><b>Frame drops on macOS</b></summary>

Usually caused by macOS WindowServer scheduling. Safari consumes a lot of compositing resources — no need to close it, just press `⌘H` to hide it and things will improve.

</details>

---

## Feedback

- **Bug Reports & Feature Requests** · [GitHub Issues](https://github.com/Eplorr/LyricsBlossom/issues)
- **QQ Group** · [Join the LyricsBlossom group chat](https://qm.qq.com/q/fz4cjWKjQc)

When reporting bugs, please include your OS version and steps to reproduce.

---

## License

**LyricsBlossom is proprietary software. All rights reserved.**

This project is closed-source software, for personal use only. Copying, modifying, distributing, or reselling without permission is prohibited.

See [LICENSE](LICENSE) for details.

</div>
