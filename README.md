# Tenebrium | Triggered Output Notification Engine (TONE)

![Antigravity Maintained](https://img.shields.io/badge/Antigravity-Maintained-blueviolet)
![Project Status](https://img.shields.io/badge/Status-Alpha_Refinement-orange)
![Version](https://img.shields.io/badge/Version-0.2.1-blue)

**TONE** (Triggered Output Notification Engine) is a sophisticated, real-time log monitoring tool designed to bridge the gap between static log files and immediate situational awareness. Whether you're tracking system errors, application events, or game logs, TONE allows you to define complex patterns that trigger custom audio alerts or Text-to-Speech (TTS) notifications.

## 🚀 Alpha Refinement
This release introduces a unified variable engine, integrated Google TTS voices, and a high-performance HUD for tracking concurrent events. TONE provides a centralized hub to manage multiple log streams, configure delayed notifications via a sophisticated timer system, and transform raw log data into spoken insights with unprecedented precision.

---

## ✨ Core Features

- **Real-time Monitoring**: Instant detection of patterns in `.log` and `.txt` files with automatic log rotation handling.
- **Advanced Pattern Management**:
  - **Inline Toggling**: Enable or disable patterns instantly via the dashboard.
  - **Visual Dimming**: Disabled patterns are visually faded to keep your workspace clear.
  - **Pattern Duplication**: Clone complex patterns to quickly iterate on notification logic.
- **Intelligent Timer System**:
  - **Delayed Playback**: Trigger notifications after a set delay.
  - **Behaviors**: Choose between `refresh`, `queue`, `ignore`, and `parallel` reset modes.
  - **HUD Tracking**: Visual progress bars with sorting (time remaining/start time) and custom formatting (HH:MM:SS, MM:SS, Decimal).
- **Dynamic Text-to-Speech (TTS)**:
  - **Google TTS Integration**: Access a wide array of international voices and accents.
  - **Per-Pattern Overrides**: Assign unique voices and volumes to specific notification types.
  - **Variable Substitution**: Speak actual log data using `{match}`, `{timestamp}`, and custom variables.
- **Unified Variable Engine**:
  - **10+ Transformations**: Clean and extract data using `strip`, `extract_between`, `replace_text`, `truncate`, and advanced regex.
  - **Custom Profile Variables**: Define global variables shared across all patterns in a profile.
- **Customizable HUD**:
  - **Overlay Mode**: A borderless, transparent HUD that stays on top of other windows.
  - **Ghost Color Transparency**: Ensures UI text remains sharp and opaque even on transparent backgrounds.
  - **Adjustable Opacity**: Fine-tune the HUD transparency to match your aesthetic.

---

## 🖥️ Dashboard Architecture

TONE features a modern, dark-themed GUI organized in a 3x3 grid for maximum efficiency:

| Panel | Function |
| :--- | :--- |
| **Log Files** | Manage the list of files to monitor across multiple profiles. |
| **Patterns** | High-level view of all patterns with inline status toggles. |
| **Global Controls**| Master volume (scaling all audio/TTS) and global cooldown. |
| **Active Timers** | The HUD control center with sorting and search facilities. |
| **Pattern Editor** | Tabbed workshop for Matching, Audio, TTS, Variables, and Timers. |
| **Tabbed Display** | Live match history and Global TTS voice/speed settings. |
| **Status Bar** | Real-time engine state and system notifications. |

---

## 🔍 Pattern Matching System

### GUI Mode
Designed for quick configuration without needing regex knowledge. Combine multiple logic operations:
- **Contains**: Look for specific keywords anywhere in the line.
- **Starts/Ends With**: Match specific prefixes or suffixes.
- **Logic Gates (Any/All)**: Trigger if any operation matches, or only if all criteria are met.

### Regex Mode
For power users, TONE supports full Python-style regular expressions. This allows for complex matching logic, case-insensitive flags `(?i)`, and capturing groups for use in variable transformations.

---

## ⏲️ Timer System & HUD

Delayed notifications allow you to track "states" rather than just "events."
- **Sorting**: Arrange active timers by urgency or chronological order.
- **Formatting**: Auto-scaling time displays (e.g., MM:SS) or high-precision decimal seconds.
- **Visuals**: Progress bars provide an at-a-glance status of all pending notifications.
- **Dismissal**: Instantly cancel individual timers or clear the entire HUD.

---

## 🗣️ Variables & Transformations

Clean up technical log data before it's spoken or displayed.
- **Built-in Variables**: Access `{match}`, `{timestamp}`, and `{log_file}` instantly.
- **Chained Transformations**: Apply multiple operations in sequence (e.g., `extract_between` -> `upper` -> `replace_text`).
- **Regex Masterclass**: Use capture groups in transformations to reformat complex strings into human-readable sentences.

---

## 📖 Compendium of Instruction

TONE includes a fully integrated, searchable in-app manual.
- **Wiki Format**: Richly formatted documentation with advanced tutorials.
- **Searchable Index**: Instantly find matching operations or transformation examples.
- **Workflow Guides**: Learn complex setups like loot filters and activity dashboards.
