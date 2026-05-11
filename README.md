# My Pure Black Theme for JetBrains IDEs

A minimal pure black theme plugin for JetBrains IDEs.

The theme is designed for users who want the IDE chrome, editor tabs, popups, notifications, progress windows, terminal, and scrollbars to stay visually consistent with a black UI instead of falling back to gray inactive states or accent-colored hover states.

## Features

- Pure black IDE frame and title areas.
- Editor tabs keep their foreground color when the IDE loses focus.
- Background task progress windows and notification popups use black headers and backgrounds.
- Scrollbars keep a neutral dark gray thumb color on hover.
- Terminal and block terminal backgrounds are pure black.
- Button focus and default-button borders use a neutral dark border instead of the default blue focus ring.

## Installation

1. Build or package the plugin JAR from this project.
2. In a JetBrains IDE, open `Settings` -> `Plugins`.
3. Click the gear icon and choose `Install Plugin from Disk...`.
4. Select the generated plugin JAR.
5. Restart the IDE.
6. Select `My-pure-black-theme-jetbrains` from `Settings` -> `Appearance & Behavior` -> `Appearance` -> `Theme`.

## Project Structure

- `resources/META-INF/plugin.xml` declares the plugin and theme provider.
- `resources/theme/mypureblackthemejetbrains.theme.json` defines the UI theme colors.
- `resources/theme/my-theme.xml` defines the editor color scheme.

## Notes

JetBrains UI theme keys can vary between IDE versions and UI implementations. Some compatibility keys are intentionally included so the theme works across newer JetBrains IDE builds that use the new UI and Islands components.
