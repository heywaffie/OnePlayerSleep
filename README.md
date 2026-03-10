# OnePlayerSleep Documentation

**OnePlayerSleep** is a lightweight, optimized Minecraft plugin that allows a single player to skip the night by sleeping, instead of requiring all players to sleep. Perfect for servers where players are spread across different areas or time zones.
**Version:** 3.6.4 
**Author:** Luno
Download: https://modrinth.com/project/RfE1BSdK
![OnePlayerSleep](https://cdn.modrinth.com/data/cached_images/48e2fa9057a8f535b9676e028629c66b4b998b2a.png)

## 📖 Overview
---

## Features

- 🌙 **One Player Sleep** - Single player can skip night for everyone
- ⚡ **Optional Weather Clearing** - Choose whether to clear rain/thunder when skipping night
- 🎨 **Fully Customizable** - Change plugin name, messages, and colors
- 🔧 **Simple Commands** - Enable, disable, reload configuration
- 👮🏻 **Permission System** - LuckPerms compatible with granular permissions
- 📊 **Message Controls** - Toggle broadcasts, command messages, console logs
- ✨ **Aesthetic UI** - Beautiful colored console messages on startup/shutdown
- 🧩 **Optimized Performance** - Message and config caching for minimal overhead
- 🌐 **Multi-Version Support** - Works on Minecraft 1.16 through 1.21+

---

## 📦 Installation

1. Download `OnePlayerSleep-xx.jar`
2. Place the JAR file in your server's `plugins/` folder
3. Restart your server (or use `/reload confirm` at your own risk)
4. Configuration file will be auto-generated at `plugins/OnePlayerSleep/config.yml`
5. Customize settings and reload with `/oneplayersleep reload`

---

## ⚙️ Configuration

### Default config.yml

```yaml
# OnePlayerSleep Configuration
# Customize your plugin settings here

# Plugin Display Name
# Change this to match your server name (e.g., GlaceSleep, DreamSleep, etc.)
plugin-name: "OnePlayerSleep"

# Enable/Disable plugin on startup
enabled-on-startup: true

# Weather Clearing
# Set to true to clear rain/thunder when skipping night
# Set to false to only skip time without affecting weather
weather-clear: false

# Message Settings
message-settings:
  # Show message when night is skipped
  show-night-skip: true
  # Show messages for enable/disable commands
  show-toggle-messages: true
  # Send messages to console
  console-logging: true

# Messages (Use & for color codes)
messages:
  night-skipped: "&6Night skipped by %player%"
  plugin-enabled: "&a%plugin% enabled!"
  plugin-disabled: "&c%plugin% disabled!"
  plugin-reloaded: "&a%plugin% configuration reloaded!"
  no-permission: "&cYou don't have permission to use this command."
  status-enabled: "&6%plugin% is currently &aenabled&6."
  status-disabled: "&6%plugin% is currently &cdisabled&6."
  usage: "&6Usage: /oneplayersleep <enable|disable|reload>"

# Do not modify this
config-version: 1
```

## 🎮 Commands

| Command | Description | Permission |
|---------|-------------|------------|
| `/oneplayersleep` | Show plugin status and usage | `oneplayersleep.toggle` |
| `/oneplayersleep enable` | Enable the plugin | `oneplayersleep.toggle` |
| `/oneplayersleep disable` | Disable the plugin | `oneplayersleep.toggle` |
| `/oneplayersleep reload` | Reload configuration | `oneplayersleep.reload` |

---

## 🔐 Permissions

| Permission | Description | Default |
|------------|-------------|---------|
| `oneplayersleep.toggle` | Allows toggling plugin on/off | OP |
| `oneplayersleep.reload` | Allows reloading configuration | OP |
| `oneplayersleep.*` | Grants all permissions | OP |

### LuckPerms Setup

Grant permission to a player:
```
/lp user <username> permission set oneplayersleep.toggle true
```

Grant permission to a group:
```
/lp group <groupname> permission set oneplayersleep.toggle true
```

Grant all permissions:
```
/lp user <username> permission set oneplayersleep.* true
```

---

## 🌍 Compatibility

### Minecraft Versions
- **1.16.x** - Fully supported
- **1.17.x** - Fully supported
- **1.18.x** - Fully supported
- **1.19.x** - Fully supported
- **1.20.x** - Fully supported
- **1.21.x** - Fully supported
- **Future versions** - Should remain compatible

### Server Software
- Spigot
- Paper (Recommended)
- Purpur
- Any Spigot-based server

### Java Versions
- Java 17 (Minimum required)
- Java 18
- Java 19
- Java 20
- Java 21 (LTS - Recommended)
- Java 22+

---

## 📊 Performance

The plugin is highly optimized:
- **Memory:** ~1MB RAM usage
- **CPU:** Minimal overhead (event-driven, cached config)
- **Startup:** <100ms load time
- **Per-event:** <1ms processing time

Optimizations include:
- Config value caching
- Message pre-processing
- Reflection method caching
- Efficient event handling

---
```

---

## ❓ FAQ

**Q: Does this work with sleeping percentage plugins?**  
A: This plugin bypasses the vanilla sleep percentage requirement entirely. It may conflict with other sleep plugins.

**Q: Can I make it require 2 players instead of 1?**  
A: Not currently. This plugin is designed specifically for single-player sleep.

**Q: Does it work in the Nether or End?**  
A: No, sleeping only works in the Overworld (normal world) as per Minecraft mechanics.

**Q: Will it work on older versions like 1.12?**  
A: No, minimum version is 1.16 due to API requirements.

**Q: Can I disable the startup messages?**  
A: Yes, set `message-settings.console-logging: false` in config.

**Q: Does weather clearing affect thunderstorms?**  
A: Yes, when `weather-clear: true`, both rain and thunder are cleared.

---

## 📜 License

MIT

---



