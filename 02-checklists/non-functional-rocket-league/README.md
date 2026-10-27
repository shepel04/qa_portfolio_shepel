# Non-functional checklist · Rocket League

[← Back to checklists](../README.md)

| Game | Platform | Checks | Types |
|---|---|---|---|
| Rocket League | PC (Epic Games) | 25 | 10 |

**Goal:** cover the game with non-functional checks of different types - not *what* the game does,
but *how well* it does it.

| Type | What it checks |
|---|---|
| Performance | FPS, loading time, memory |
| Compatibility | OS versions, controllers, resolutions, refresh rates |
| Usability | Controller navigation, rebinding, readability |
| Localization | Long strings, language switching |
| Network | High ping, reconnect, connection warnings |
| Installation & update | Install from launcher, settings after update |
| Security | Login required, chat filter |
| Accessibility | Colorblind players, text size |
| Audio | Volume channels |
| Stability & recovery | Alt+Tab, force close |

📄 [checklist.xlsx](checklist.xlsx) · [Google Sheets](https://docs.google.com/spreadsheets/d/1I3fSWyucftm2tldW_8a010RV_gJs2XAhovh_i8H6Zrk/edit)

### Performance

| ID | Priority | Summary | Status | Issue | Comment |
|---|---|---|---|---|---|
| TC-1 | High | Verify the game keeps stable 60 FPS in a 3v3 online match on recommended specs (High settings) | Passed |  |  |
| TC-2 | Medium | Verify the main menu opens within 15 seconds after the game launch | Passed |  |  |
| TC-3 | Medium | Verify loading into a match takes no longer than 10 seconds | Passed |  |  |
| TC-4 | Medium | Verify RAM usage does not keep growing after 5 matches in a row | Passed |  |  |

### Compatibility

| ID | Priority | Summary | Status | Issue | Comment |
|---|---|---|---|---|---|
| TC-5 | High | Verify the game launches and runs on Windows 10 and Windows 11 | Passed |  |  |
| TC-6 | High | Verify Xbox and PlayStation controllers are detected and work in menus and matches | Passed |  |  |
| TC-7 | Medium | Verify the game displays correctly in 16:9 and 21:9 resolutions | Passed |  |  |
| TC-8 | Low | Verify the game works correctly on 60 Hz and 144 Hz monitors | Passed |  |  |

### Usability

| ID | Priority | Summary | Status | Issue | Comment |
|---|---|---|---|---|---|
| TC-9 | High | Verify all main menu items can be reached using only a controller | Passed |  |  |
| TC-10 | Medium | Verify controls can be rebound and the new bindings are saved after restart | Passed |  |  |
| TC-11 | Low | Verify UI text is readable at 1280x720 resolution | Passed |  |  |

### Localization

| ID | Priority | Summary | Status | Issue | Comment |
|---|---|---|---|---|---|
| TC-12 | Medium | Verify UI text fits inside buttons in German and Polish (long strings) | Passed |  |  |
| TC-13 | Low | Verify changing the game language applies to all menus | Passed |  |  |

### Network

| ID | Priority | Summary | Status | Issue | Comment |
|---|---|---|---|---|---|
| TC-14 | High | Verify the match stays playable with 150 ms ping | Passed |  |  |
| TC-15 | High | Verify the game reconnects to the match after a 10 second internet loss | Passed |  |  |
| TC-16 | Medium | Verify the network warning icon appears when the connection is unstable | Passed |  |  |

### Installation & update

| ID | Priority | Summary | Status | Issue | Comment |
|---|---|---|---|---|---|
| TC-17 | High | Verify the game installs and launches from the Epic Games Launcher | Passed |  |  |
| TC-18 | Medium | Verify settings are kept after a game update | Passed |  |  |

### Security

| ID | Priority | Summary | Status | Issue | Comment |
|---|---|---|---|---|---|
| TC-19 | High | Verify the game cannot be played online without logging in to an Epic account | Passed |  |  |
| TC-20 | Medium | Verify the chat filter hides offensive words | Passed |  |  |

### Accessibility

| ID | Priority | Summary | Status | Issue | Comment |
|---|---|---|---|---|---|
| TC-21 | Medium | Verify team colors can be told apart by colorblind players | Passed |  |  |
| TC-22 | Low | Verify chat and quick chat text size is readable | Passed |  |  |

### Audio

| ID | Priority | Summary | Status | Issue | Comment |
|---|---|---|---|---|---|
| TC-23 | Medium | Verify master, music and effects volume sliders work independently | Passed |  |  |

### Stability & recovery

| ID | Priority | Summary | Status | Issue | Comment |
|---|---|---|---|---|---|
| TC-24 | High | Verify the game recovers correctly after Alt+Tab during a match | Passed |  |  |
| TC-25 | Medium | Verify settings are not lost after the game is force closed | Passed |  |  |
