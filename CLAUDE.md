# Ship Studio Project

This is an Expo (React Native) mobile app on **Expo SDK 55**. You're helping a **non-developer** build an iOS/Android app. Keep explanations simple and jargon-free.

When you need Expo APIs, read the versioned docs at https://docs.expo.dev/versions/v55.0.0/ — Expo changes fast and older knowledge may be stale.

---

## Environment: Ship Studio App

You are running inside the **Ship Studio app**, which handles the development environment automatically.

**Important things to know:**

- Ship Studio shows the app on a **real iOS Simulator (or Android emulator)** in the preview pane
- The app is **built and launched automatically** when the project opens — do NOT run `npx expo start`, `npx expo run:ios`, or any build/run commands
- The first build takes a few minutes; the build log streams inside the preview pane
- After saving a file, the running app **fast-refreshes automatically** within a moment or two
- If the app looks stuck, tell the user to click **Reload** in the preview toolbar

**If the user says they can't see their app or the preview isn't working:**
> "Try clicking the **Projects** button in the top right corner to go back to the project list, then reopen your project. This restarts the preview."

---

## FIRST: Check for Onboarding

**Before doing anything else**, check if `APP.md` exists.

- If `APP.md` **does NOT exist**: Ask the user what they want their app to do, who it's for, and how it should feel. Create `APP.md` with their answers, including app purpose, screens plan, brand personality, and colors.
- If `APP.md` **exists**: Read it to understand the project before making changes.

---

## Project Structure

```
App.tsx          # The app — every screen starts here
app.json         # App name, icon, splash screen, platform config
assets/          # Icons and images
index.ts         # Entry point (don't touch)
```

There is no `ios/` or `android/` folder — Expo generates them on demand. Never create or edit native folders by hand; configure everything through `app.json`.

---

## Working in This Project

- **Keep dependencies minimal.** Prefer React Native built-ins. When you need more, prefer Expo SDK packages installed with `npx expo install <package>` over bare npm installs — they're version-matched to this project.
- **Pure JS/TS changes** (components, styles, logic) apply via fast refresh — no rebuild.
- **Adding native dependencies or editing `app.json`** requires a rebuild: tell the user to go back to Projects and reopen the project so Ship Studio rebuilds the app.
- **Styling**: use `StyleSheet.create` like `App.tsx` does. Support dark mode via `useColorScheme()` — the starter screen shows the pattern.
- **Navigation**: when the app grows past one screen, add `@react-navigation/native` (ask before adding it).
- Update `APP.md` after meaningful changes so the project stays documented.

---

## Mobile Design Principles

- Design for one hand: primary actions near the bottom of the screen
- Respect safe areas (notches, home indicator)
- Touch targets at least 44pt
- Always handle both light and dark mode
- Use platform conventions — iOS users expect iOS patterns
