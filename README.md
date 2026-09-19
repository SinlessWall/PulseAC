# ⚡ PulseAC

**PulseAC** is a modern, lightweight, and highly configurable Minecraft anti-cheat designed to detect and prevent unfair gameplay while keeping server performance and player experience in mind.

PulseAC provides a complete detection and staff-management system, including combat checks, movement checks, clicking checks, violation tracking, staff alerts, player profiles, spectating tools, client information, setbacks, bypass permissions, and more.

The system is designed to be modular and configurable, allowing server owners to enable the checks and features that best fit their server.

---

# 🛡️ Features

PulseAC includes a wide range of tools for both **detection** and **staff moderation**.

### ⚔️ Combat Detection

* KillAura detection
* Reach detection
* Attack pattern analysis
* Invalid attack detection
* Suspicious target switching
* Abnormal hit timing
* Combat violation tracking

### 🏃 Movement Detection

* Speed detection
* Fly detection
* NoFall detection
* Phase detection
* Jesus detection
* Invalid movement detection
* Abnormal acceleration detection
* Movement violation tracking

### 🖱️ Click Detection

* CPS monitoring
* AutoClicker detection
* Abnormal click patterns
* Consistent click interval detection
* Configurable CPS limits
* Click violation tracking

### 📦 Player & Gameplay Checks

PulseAC is designed around a modular check system, allowing additional detections to be added without changing the entire anti-cheat.

Checks can have their own:

* Detection logic
* Violation levels
* Thresholds
* Alerts
* Setbacks
* Punishment actions
* Configuration options

---

# 🔍 Checks

PulseAC organizes detections into individual checks, allowing server owners to control and configure their anti-cheat more easily.

| Category     | Checks                               |
| ------------ | ------------------------------------ |
| ⚔️ Combat    | KillAura, Reach, InvalidAttack       |
| 🏃 Movement  | Speed, Fly, NoFall, Phase, Jesus     |
| 🖱️ Clicking | CPS, AutoClicker, Click Patterns     |
| 👤 Player    | Invalid Movement, Abnormal Behaviour |

Each check can be configured independently depending on the server's requirements.

More checks can be added as PulseAC continues to develop.

---

# 🚨 Violation System

PulseAC uses a **Violation Level (VL)** system to track suspicious behaviour.

When a player triggers a detection, their violation level can increase.

A typical detection process can look like:

```text
Detection
   ↓
Flag
   ↓
Violation Level Increase
   ↓
Staff Alert
   ↓
Setback
   ↓
Configured Action
```

Server owners can configure how many violations are required before different actions are taken.

This allows PulseAC to respond differently to individual suspicious events and repeated violations.

---

# 👮 Staff System

PulseAC includes several commands and permissions designed specifically for server staff.

### `Pulse.staff`

Allows authorized staff members to access PulseAC staff functionality.

This can be used as the main permission for staff-related PulseAC features.

### `Pulse.alerts`

Allows staff members to receive real-time anti-cheat alerts.

Alerts can contain information such as:

* Player
* Check
* Violation level
* Detection information
* Action taken

### `Pulse.verbose`

Provides detailed detection information for staff and administrators.

Verbose mode can be useful when:

* Testing checks
* Investigating false positives
* Debugging detections
* Developing new checks
* Reviewing suspicious behaviour

---

# 👁️ Spectate System

PulseAC provides staff with tools for monitoring suspicious players.

### `Pulse.spectate`

Allows authorized staff members to spectate players being investigated.

This can be useful for manually verifying suspicious behaviour before taking further action.

### `Pulse.stopspectating`

Allows staff members to stop spectating a player and return to their normal state.

Together, these commands provide a simple way for staff to investigate suspicious players directly in-game.

---

# 👤 Player Profiles

### `Pulse.profile`

PulseAC can provide staff with information about a player's anti-cheat profile.

A profile can contain information such as:

* Player name
* Violation levels
* Triggered checks
* Detection history
* Client information
* Current status
* Recent alerts

This gives staff a quick overview when investigating a player.

---

# 💻 Client Brand Detection

### `Pulse.clientbrand`

PulseAC can retrieve and display the Minecraft client brand reported by a player.

Client brand information can help staff investigate suspicious behaviour alongside actual anti-cheat detections.

> **Important:** Client brand information by itself should not be treated as proof that a player is cheating.

---

# 🔄 Setback System

PulseAC supports configurable setbacks for checks where returning a player to a previous legitimate position is appropriate.

Setbacks can be useful for movement-related detections by preventing players from continuing abnormal movement.

### `Pulse.nosetback`

Allows authorized staff or configured users to bypass PulseAC setbacks.

This can be useful for:

* Staff members
* Developers
* Testing accounts
* Debugging
* Special server environments

Setback bypasses should be given carefully because they can prevent detections from correcting abnormal movement.

---

# 🛡️ Bypass System

### `Pulse.bypass`

Allows authorized players to bypass configured PulseAC detections.

This permission can be useful for:

* Staff
* Developers
* Testing accounts
* Server administrators
* Anti-cheat testing

Bypass permissions should only be given to trusted users because bypassing checks can allow behaviour that would normally trigger detections.

---

# 🔔 Staff Alerts

PulseAC provides real-time alerts to staff members with the appropriate permissions.

A typical alert can contain:

```text
PulseAC | Player: ExamplePlayer
Check: Speed
VL: 4
Detection: Abnormal Movement
Action: Setback
```

The alert system can be customized through the configuration.

---

# 👁️ Investigation Tools

PulseAC isn't designed to rely exclusively on automatic punishments.

Staff can investigate suspicious players using:

* Anti-cheat alerts
* Verbose information
* Player profiles
* Spectating
* Client brand information
* Violation levels
* Detection history

This allows server staff to combine automated detection with manual investigation.

---

# ⚙️ Configuration

PulseAC is designed to be highly configurable.

Server owners can customize:

* Enabled checks
* Check thresholds
* Violation levels
* Detection sensitivity
* Setbacks
* Punishments
* Staff alerts
* Verbose messages
* Prefixes
* Permissions
* Messages
* Client information
* Bypass settings

Individual checks can be adjusted without changing the entire anti-cheat.

---

# 🚀 Performance

PulseAC is designed with server performance in mind.

The goal is to continuously monitor player behaviour without creating unnecessary server overhead.

PulseAC focuses on:

* Efficient detection
* Modular checks
* Configurable processing
* Lightweight monitoring
* Scalable player tracking
* Minimal unnecessary processing

---

# 🧩 Modular Architecture

PulseAC uses a modular check system.

This makes it possible to add new detections while keeping existing features organized.

Each check can have its own:

* Detection system
* Configuration
* Violation handling
* Alert format
* Setback behaviour
* Punishment settings

This makes PulseAC easier to expand and maintain as the project grows.

---

# 🖥️ Compatibility

PulseAC is designed to support modern **Bukkit-based Minecraft server software**, with compatibility ranging from **Minecraft 1.8.8 through 1.21.x**.

## Supported Server Software

| Server Software | Compatibility  | Notes                                                                              |
| --------------- | -------------- | ---------------------------------------------------------------------------------- |
| **Paper**       | 🌟 Recommended | Optimized for Paper's event system and packet handling.                            |
| **Purpur**      | 🌟 Recommended | Fully compatible and ideal for SMP servers.                                        |
| **Pufferfish**  | 🌟 Recommended | Compatible with high-performance Paper-based environments.                         |
| **Folia**       | ✅ Supported    | Supports Folia's regionized scheduling architecture when configured appropriately. |
| **Spigot**      | ✅ Supported    | Supports standard Spigot environments.                                             |
| **CraftBukkit** | ✅ Supported    | Supports Bukkit/CraftBukkit-based servers, including legacy environments.          |

---

# ☕ Java Requirements

PulseAC requires a supported Java runtime appropriate for the Minecraft server version being used.

### Recommended Java Versions

* **Java 17**
* **Java 21**

For modern Paper and Purpur versions, **Java 21** is recommended where supported by the server version.

| Minecraft Version  | Recommended Java            |
| ------------------ | --------------------------- |
| **1.8.8 – 1.16.x** | Java 8 / compatible runtime |
| **1.17 – 1.20.4**  | Java 17                     |
| **1.20.5+**        | Java 21                     |
| **1.21.x**         | Java 21                     |

> **Note:** The required Java version is primarily determined by the Minecraft server software and Minecraft version.

---

# 📦 Installation

PulseAC is installed as a standard Minecraft server plugin.

### Installation Steps

1. Download the PulseAC `.jar`.
2. Place it inside your server's `plugins` folder.
3. Restart the server.
4. Open the generated PulseAC configuration.
5. Configure the checks you want to use.
6. Configure staff permissions and alerts.
7. Test the configuration.
8. Enable automatic punishments only after testing.

Example:

```text
/server
├── plugins/
│   ├── PulseAC.jar
│   └── ...
├── server.properties
└── ...
```

---

# 📋 Commands & Permissions

| Permission             | Purpose                                |
| ---------------------- | -------------------------------------- |
| `Pulse.staff`          | Access PulseAC staff functionality     |
| `Pulse.alerts`         | Receive anti-cheat alerts              |
| `Pulse.verbose`        | View detailed detection information    |
| `Pulse.spectate`       | Spectate players for investigation     |
| `Pulse.stopspectating` | Stop spectating a player               |
| `Pulse.profile`        | View player anti-cheat profiles        |
| `Pulse.clientbrand`    | View reported client brand information |
| `Pulse.nosetback`      | Bypass PulseAC setbacks                |
| `Pulse.bypass`         | Bypass configured PulseAC checks       |

---

# 🔮 Future Development

PulseAC is designed to continue expanding with new checks, improvements, and administration features.

Potential future additions include:

* More advanced combat checks
* Improved movement analysis
* Additional inventory checks
* Better packet analysis
* Advanced reach analysis
* Improved AutoClicker detection
* More false-positive prevention
* Expanded staff tools
* Web-based statistics
* Detection logs
* API support
* Developer API
* More configurable punishments
* Improved player profiles
* Additional investigation tools

---

# 🤝 Bug Reports & Contributions

If you discover a problem with PulseAC, please report it with as much information as possible.

Useful information includes:

* Minecraft version
* Server software
* PulseAC version
* Check that triggered
* Player behaviour
* Console output
* Configuration
* Steps to reproduce the issue

False positives should also be reported so detection systems can be investigated and improved.

---

# ⚠️ Disclaimer

No anti-cheat can guarantee perfect detection.

Minecraft has many legitimate gameplay situations, different network conditions, server configurations, client behaviours, and unusual interactions that can affect detection systems.

PulseAC should be properly configured and tested before enabling automatic punishments.

Server owners are responsible for reviewing their configuration and deciding how violations should be handled.

---

# 📜 Terms of Service

By downloading, installing, or using **PulseAC**, you acknowledge that you have read, understood, and agreed to the PulseAC **Terms of Service (ToS)**.

Your use of PulseAC is subject to the rules and conditions outlined in the official PulseAC ToS.

If you do not agree with the Terms of Service, **do not download, install, or use PulseAC**.

By continuing to use PulseAC, you agree that:

* You will use PulseAC responsibly and for legitimate server administration purposes.
* You are responsible for configuring PulseAC correctly for your server.
* You understand that no anti-cheat can guarantee 100% detection accuracy.
* You are responsible for reviewing detections before applying automatic punishments.
* You will not intentionally use PulseAC to cause harm to other servers, players, or systems.
* You will comply with applicable laws and the rules of the Minecraft server software you are using.
* PulseAC developers are not responsible for server issues, configuration mistakes, false positives, player punishments, or other consequences resulting from the use or configuration of the plugin.

> **By downloading or using PulseAC, you agree to these Terms of Service.**

> **If you do not agree to these terms, please do not download or use PulseAC.**

**© PulseAC — All rights reserved.**
