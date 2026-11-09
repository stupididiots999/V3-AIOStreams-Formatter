<div align="center">

# ✨ V3 AIOStreams Formatter

![Version](https://img.shields.io/badge/version-v3.0-blue.svg?style=for-the-badge)
![Platform](https://img.shields.io/badge/platform-AIOStreams-success.svg?style=for-the-badge)
![Status](https://img.shields.io/badge/status-active-success.svg?style=for-the-badge)

*A cleaner, smarter V3 AIOStreams custom formatter. Automatically hides redundant tags, detects Open Matte & special editions, fixes double-spacing, and smartly displays filenames for AI or unknown streams.*

</div>

---

## 🏷️ Name Template Changes

### 🧠 Smart 10-bit Logic
The `10bit` tag (🖍️) is now dynamically hidden if HDR or Dolby Vision is already detected. It will only display for 10-bit SDR files, keeping your titles uncluttered and avoiding redundant information.

### 🖼️ Open Matte Detection
Actively scans file and folder names for multiple variations of "Open Matte" (e.g., `Open.Matte`, `openmatte`) and automatically flags them with:
` • 🖼️ Open Matte`

### 🧹 Cleaner Display
Redundant text like "Color Corrected" is automatically filtered and stripped out so it doesn't clutter the title.

### ↔️ Dynamic Spacing
Fixed the awkward double-spacing issues by integrating spaces and bullet points *directly* into the tags themselves. 

> **Example:** In the old format, there were hardcoded spaces between the major blocks (like between Resolution and Visual Tags). If a file didn't have visual tags, you were left with a weird double space. Now, those hardcoded gaps are gone. The spacing is built right into the replacement (e.g., formatting HDR as ` • 🎨 HDR`). If the tag doesn't exist, its extra space is completely removed, ensuring a perfectly clean line every time.

### 🎬 Expanded Edition Tags
Added advanced detection and custom emojis for several editions that were previously missing from the standard format:

* 🪄 **Remastered**
* 📚 **Collector’s**
* 🎉 **Anniversary**
* ✂️ **Uncut**
* 😈 **Unrated**
* 🌶️ **Uncensored**

---

## 📝 Description Template Changes

### 📉 Decluttered Title Line
Completely removed the Seadex and RSE tiering logic (🎚️ Best, T1-T8). The top line now strictly focuses on the **Title**, **Year**, **Seasons**, and **Episodes** for a much cleaner, easier-to-read look.

### 📄 Smart Filename Display
The description now automatically shows the raw filename (`📄 {stream.filename}`) at the very bottom in **two specific situations** to give you better context:

1. **For "AI" Releases:** "AI" is a broad term—it could mean AI-upscaled, AI 60fps interpolation, or an AI-generated Open Matte. Because release groups rarely write what they did with AI in a standard format that AIOStreams can automatically read, printing the filename is the easiest way to let you see exactly what you are clicking on.
2. **For Unknown Resolutions:** When a file is missing a resolution tag, the filename often holds the missing visual clues. These files actually often have Dolby Vision (DV) or HDR tags in the name, just not the resolution. If you see a massive 50–70 GB file with an "Unknown" resolution, glancing at the raw filename for those DV/HDR clues lets you safely conclude it must be a 4K release and is perfectly usable.

---

## 🔗 Links & Installation

To use this formatting, paste the following Raw links into your AIOStreams settings:

**Name Template:**
```text
[https://pastebin.com/raw/XPehQTCV](https://pastebin.com/raw/XPehQTCV)
