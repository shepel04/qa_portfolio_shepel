<div align="center">

# 🎮 Game QA Portfolio

**Taras Shepel** · Game QA Engineer · Cherkasy, Ukraine

![Android](https://img.shields.io/badge/Android-3DDC84?style=flat&logo=android&logoColor=white)
![PC](https://img.shields.io/badge/PC-0078D6?style=flat&logo=windows&logoColor=white)
![adb](https://img.shields.io/badge/adb-34A853?style=flat&logo=android&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Google Sheets](https://img.shields.io/badge/Google%20Sheets-34A853?style=flat&logo=googlesheets&logoColor=white)
![Jira](https://img.shields.io/badge/Jira-0052CC?style=flat&logo=jira&logoColor=white)

[LinkedIn](https://linkedin.com/in/your-profile) · [Email](mailto:your@email.com) · [perfgrab tool](https://github.com/your-username/perfgrab)

</div>

---

## 👋 About

<!-- 2-3 sentences. Keep it short. -->
Game QA engineer with a Python automation background. I test mobile and PC games: functional,
interruption, performance, compatibility and balance testing. I also build my own QA tools -
see [perfgrab](https://github.com/your-username/perfgrab), a desktop app for automated performance
and interruption testing of Android games over adb.

**Core skills:** test design (checklists, test cases, pairwise) · bug reporting · performance testing ·
interruption testing · requirements analysis · adb · Python automation

---

## 📂 Contents

| # | Section | Game / Platform | Highlights |
|---|---|---|---|
| 01 | [Bug reports](01-bug-reports/) | <!-- games --> | <!-- e.g. 8 bugs, 2 critical --> |
| 02 | [Interruption checklist](02-checklists/interruptions-tank-busters/) | Tank Busters · Android | 16 checks, 13 automated via adb |
| 03 | [Non-functional checklist](02-checklists/non-functional-rocket-league/) | Rocket League · PC | 25 checks, 10 test types |
| 04 | [Pairwise testing](03-test-design/pairwise-rocket-league/) | Rocket League · PC | 16 cases instead of 96 |
| 05 | [Performance testing](04-performance-testing/) | <!-- game --> · Android | FPS, CPU, GPU, RAM, temperature |
| 06 | [Balance testing](05-balance-testing/) | <!-- game --> · Android | 10 runs of one level, moves left |
| 07 | [Requirements analysis](06-requirements-analysis/) | - | Bad → good requirements |
| 08 | [Localization](07-localization/) | - | Lockit, text overflow checks |
| 🛠 | [perfgrab](https://github.com/your-username/perfgrab) | Android | My own QA tool |

---

## 🐞 01 · Bug reports

<!-- The most important section. 5-8 best bugs, each with a video or GIF. -->

| ID | Summary | Game | Severity | Priority | Evidence |
|---|---|---|---|---|---|
| BUG-1 | <!-- What? Where? When? --> | <!-- game --> | Major | High | [video](link) |
| BUG-2 | | | Minor | Medium | [video](link) |
| BUG-3 | | | Critical | Urgent | [video](link) |

<details>
<summary><b>BUG-1 · Example of a full report</b></summary>

| Field | Value |
|---|---|
| **Summary** | <!-- e.g. Game crashes after returning from Recent apps during a battle --> |
| **Steps to reproduce** | 1. Launch the game<br>2. Start a battle<br>3. Open Recent apps<br>4. Return to the game |
| **Actual result** | <!-- --> |
| **Expected result** | <!-- --> |
| **Device** | <!-- Samsung Galaxy A55, Android 14 --> |
| **Build** | <!-- 1.2.3 (45) --> |
| **Severity / Priority** | Critical / High |
| **Attachments** | [video](link) · [logcat](link) |

</details>

---

## ✅ 02 · Interruption checklist - Tank Busters

| Game | Platform | Device | Tools |
|---|---|---|---|
| Tank Busters | Android | <!-- device --> | adb, perfgrab |

**Task:** check how the game handles interruptions - calls, notifications, Home, lock screen, network loss, battery events.
**Approach:** 16 checks in 5 categories. 13 triggered automatically over adb, 1 assisted, 2 manual.
**Result:** <!-- e.g. 14 Passed · 2 Failed → BUG-3, BUG-4 -->

📄 [Checklist (Google Sheets)](link) · 📊 [Run report](02-checklists/interruptions-tank-busters/report.md)

![Interruption run](assets/interruptions-run.png)

---

## ✅ 03 · Non-functional checklist - Rocket League

| Game | Platform | Test types |
|---|---|---|
| Rocket League | PC (Epic Games) | Performance · Compatibility · Usability · Localization · Network · Installation · Security · Accessibility · Audio · Stability |

**Task:** build a checklist with non-functional checks of different types.
**Result:** 25 checks, prioritized High / Medium / Low.

📄 [Checklist (Google Sheets)](https://docs.google.com/spreadsheets/d/1I3fSWyucftm2tldW_8a010RV_gJs2XAhovh_i8H6Zrk/edit)

---

## 🧮 04 · Pairwise testing - Rocket League

**Parameters (3-4-4-2):**

| Game mode | Car body | Arena | Playlist |
|---|---|---|---|
| Duel (1v1) | Octane | DFH Stadium | Casual |
| Doubles (2v2) | Dominus | Mannfield | Competitive |
| Standard (3v3) | Fennec | Champions Field | |
| | Breakout | Urban Central | |

- All combinations: 3 × 4 × 4 × 2 = **96**
- Pairwise: 4 × 4 = **16** (two largest groups) - every pair of values appears at least once

> [!TIP]
> Most defects come from a single parameter or an interaction of two. Pairwise covers all of them with 6× fewer test runs.

📄 [Pairwise table (Google Sheets)](https://docs.google.com/spreadsheets/d/1YwYVJbzzYSanFifmXo1UiStdeNZvo067SmT_NqpbhKs/edit)

---

## 📈 05 · Performance testing

| Game | Device | Settings | Duration | Tool |
|---|---|---|---|---|
| <!-- game --> | <!-- device --> | <!-- High --> | 30 min | perfgrab (adb) |

| Avg FPS | Min / Max FPS | Avg CPU | Avg GPU | RAM | 1st / 2nd launch | Battery °C (start → 30 min) |
|---|---|---|---|---|---|---|
| <!-- --> | <!-- --> | <!-- --> | <!-- --> | <!-- MB --> | <!-- s --> | <!-- --> |

![FPS chart](assets/performance-chart.png)

**Conclusion:** <!-- 1-2 sentences: stable or not, where FPS drops, does the phone overheat -->

---

## ⚖️ 06 · Balance testing

**Task:** play the same level 10 times without boosters and record moves left.

| Game | Level | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | Avg |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| <!-- game --> | <!-- --> | | | | | | | | | | | |

**Conclusion:** <!-- is the level too easy / too hard / balanced? -->

---

## 📋 07 · Requirements analysis

| Bad requirement | Problem | Good requirement |
|---|---|---|
| The loading screen should feel fast | Not testable | The main menu opens within ≤ 10 s on min-spec devices |
| <!-- --> | <!-- --> | <!-- --> |

---

## 🌍 08 · Localization

<!-- Lockit example, text overflow screenshots, checked languages -->

---

## 🛠 Tools I built

### [perfgrab](https://github.com/your-username/perfgrab) - Android game QA toolkit

- **Performance:** auto-launch, cold start time, FPS / CPU / GPU / RAM / temperature, results ready for the test sheet
- **Interruptions:** loads any xlsx checklist, triggers interruptions over adb, auto-checks crashes / restarts / background audio, fills the checklist and writes a run report

![perfgrab](assets/perfgrab.gif)

---

## 🧰 Tools & tech

**Testing:** adb, Android Developer options, logcat, Google Sheets, Jira
**Automation:** Python, PySide6, Playwright
**Devices:** <!-- your phones / PC specs -->

---

<div align="center">

📫 Open to Game QA opportunities · [LinkedIn](https://linkedin.com/in/your-profile) · [Email](mailto:your@email.com)

</div>