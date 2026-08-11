# Abyss Theme for JetBrains

## What This Project Is

Abyss Theme for JetBrains is a resource-only UI theme plugin for JetBrains IDEs. It keeps the IDE frame, editor tabs, tool windows, popups, notifications, terminals, and supporting controls consistently dark instead of falling back to gray inactive states or bright platform defaults.

For VS Code, use [Abyss Theme for VS Code](https://github.com/jadchene/abyss-theme-for-vscode).

## Why Use It

- Pure-black IDE frame, title areas, panels, terminals, and popup headers.
- Consistent active and inactive editor-tab foregrounds.
- Neutral selection, hover, border, focus, and scrollbar states.
- Dark progress windows, notifications, menus, lists, tables, and input controls.
- Bundled editor scheme with JetBrains Mono and Microsoft YaHei UI font preferences.
- Compatibility keys for newer JetBrains UI and Islands components.

## Quick Start

Create an installable plugin JAR with a JDK:

```powershell
jar cf abyss-theme-for-jetbrains.jar -C resources .
```

Then install it:

1. Open **Settings** > **Plugins** in a JetBrains IDE.
2. Open the gear menu and choose **Install Plugin from Disk...**.
3. Select `abyss-theme-for-jetbrains.jar` and restart the IDE.
4. Open **Settings** > **Appearance & Behavior** > **Appearance**.
5. Select **Abyss Theme for JetBrains** as the theme.

## Reference

| Item | Value |
| --- | --- |
| Plugin ID | `abyss-theme-for-jetbrains` |
| Plugin version | `1.0.1` |
| Minimum platform build | `251` |
| Theme name | `Abyss Theme for JetBrains` |
| Theme author | `chenjd` |
| Editor scheme | `Abyss Theme` |
| License | MIT |

The repository intentionally contains only plugin resources; it does not require a Gradle project for local packaging.

## Development

- `resources/META-INF/plugin.xml` defines plugin metadata and registers the theme provider.
- `resources/META-INF/pluginIcon.svg` provides the plugin icon.
- `resources/theme/abyss-theme.theme.json` defines UI colors and component styling.
- `resources/theme/abyss-editor.xml` defines editor and console colors, fonts, and syntax attributes.

Validate the metadata before packaging:

```powershell
Get-Content -Raw resources/theme/abyss-theme.theme.json | ConvertFrom-Json | Out-Null
[xml](Get-Content -Raw resources/META-INF/plugin.xml) | Out-Null
[xml](Get-Content -Raw resources/theme/abyss-editor.xml) | Out-Null
```

## License

Licensed under the [MIT License](LICENSE).
