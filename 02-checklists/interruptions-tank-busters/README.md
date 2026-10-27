# Interruption checklist · Tank Busters

[← Back to checklists](../README.md)

| Game | Platform | Device | Build | Tools |
|---|---|---|---|---|
| Tank Busters | Android | Samsung Galaxy S23 (SM-S911B), Android 16 | 1.0.7 (101) | adb, [perfgrab](https://github.com/shepel04/Perfgrab) |

**Goal:** check that the game handles interruptions correctly - pauses, keeps its state, doesn't crash
and doesn't play sound in the background.

**Approach:** 16 checks in 5 categories. Run with perfgrab: 13 interruptions triggered automatically
over adb, 1 assisted (game state set by the tester), 2 manual (incoming call, wired headphones).
After each interruption the tool checks logcat for crashes/ANR, process restart, foreground state,
background audio and rendering, and saves screenshots before/after.

**Result:** 16 of 16 checks run in 26.7 min · **15 Passed · 1 Failed** · pass rate 94%.

**Failed - TC-8:** the game does not enter pause mode when the alarm goes off → [BUG-004](../../01-bug-reports/BUG-004.md).

| Before the alarm | After dismissing the alarm |
|---|---|
| <img src="../../assets/interruptions-tc8-before.jpg" width="260"> | <img src="../../assets/interruptions-tc8-after.jpg" width="260"> |

📄 [checklist.xlsx](checklist.xlsx) · 📊 [Run report](report.md)

### App lifecycle

| ID | Priority | Summary | Status | Issue | Comment |
|---|---|---|---|---|---|
| TC-1 | High | Verify the game pauses after pressing Home during gameplay and resumes in the same state | Passed |  |  |
| TC-2 | High | Verify switching to another app via Recent apps during gameplay and back keeps the game state | Passed |  |  |
| TC-3 | High | Verify locking the screen (power button) during gameplay and unlocking resumes the game | Passed |  |  |
| TC-4 | Medium | Verify pulling down the notification shade during gameplay does not break the game | Passed |  |  |
| TC-5 | High | Verify progress is saved after force-closing the game from Recent apps after finishing a level | Passed |  |  |

### Incoming events

| ID | Priority | Summary | Status | Issue | Comment |
|---|---|---|---|---|---|
| TC-6 | High | Verify the game pauses on an incoming call and resumes in the same state after declining the call | Passed |  |  |
| TC-7 | Medium | Verify an incoming push notification does not pause or break the gameplay | Passed |  |  |
| TC-8 | Medium | Verify the game pauses when the alarm/timer goes off and resumes after dismissing it | **Failed** | [BUG-004](../../01-bug-reports/BUG-004.md) | The game does not enter pause mode |
| TC-9 | Low | Verify the low battery system popup does not break the game | Passed |  |  |

### Network

| ID | Priority | Summary | Status | Issue | Comment |
|---|---|---|---|---|---|
| TC-10 | High | Verify the game handles Wi-Fi turned off during gameplay | Passed |  |  |
| TC-11 | Medium | Verify the game handles Airplane mode turned on during gameplay | Passed |  |  |

### Audio & device

| ID | Priority | Summary | Status | Issue | Comment |
|---|---|---|---|---|---|
| TC-12 | Medium | Verify the game sound switches correctly when wired headphones are plugged in / out | Passed |  |  |
| TC-13 | Low | Verify connecting / disconnecting the charger during gameplay does not affect the game | Passed |  |  |
| TC-14 | Low | Verify screen rotation with auto-rotate on does not break the UI | Passed |  |  |

### Critical moments

| ID | Priority | Summary | Status | Issue | Comment |
|---|---|---|---|---|---|
| TC-15 | High | Verify an interruption (Home) during the loading screen does not cause a crash or infinite loading | Passed |  |  |
| TC-16 | High | Verify an interruption at the end of a level (results screen) keeps the level result | Passed |  |  |
