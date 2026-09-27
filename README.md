# Dial-In Trivia — Native Android Game

A pass-and-play trivia game for groups, built with Kotlin + Jetpack Compose.

## Accessibility
- Fully usable with **TalkBack** (every control has a spoken label, results and
  feedback are announced via live regions).
- **Read-aloud is optional and off by default** — toggle it on the setup screen.
- A short tone plays on every answer (correct/incorrect) regardless of the
  read-aloud setting, so outcomes are always audible.
- Large tap targets, high-contrast color palette.

## How to build it
1. Install [Android Studio](https://developer.android.com/studio) (free).
2. Open this folder (`DialInTrivia`) as a project — "File → Open".
3. Let Gradle sync (first sync downloads dependencies, needs internet).
4. Connect an Android phone (USB debugging on) or start an emulator.
5. Click **Run ▶**.

If Android Studio prompts you to upgrade the Android Gradle Plugin or Kotlin
version, accept it — the versions pinned here are just a known-working
baseline as of early 2026.

## Project layout
- `app/src/main/java/com/dialin/trivia/MainActivity.kt` — all game logic and UI
- `app/src/main/AndroidManifest.xml` — app entry point
- `app/build.gradle.kts` — dependencies (Compose, Material3, core-ktx)

## Customizing
- Add more questions: extend the `QUESTION_BANK` list in `MainActivity.kt`
  (category, question text, 4 options, index of the correct one).
- Change the round length: edit `.take(12)` in `DialInTriviaApp`.
- Change colors: edit the color constants near the top of `MainActivity.kt`.
