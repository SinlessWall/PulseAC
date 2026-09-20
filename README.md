# ⚡ PulseAC

**PulseAC** is a modern, lightweight, and highly configurable Minecraft anti-cheat designed to detect and prevent unfair gameplay while keeping server performance and player experience in mind.

PulseAC provides a complete detection and staff-management system, featuring combat checks, movement checks, clicking checks, violation tracking, staff alerts, player profiles, spectating tools, client brand detection, setbacks, bypass permissions, and more.

Built with a modular design, PulseAC allows server owners to configure individual checks and customize how detections are handled.

---

# 🛡️ Features

PulseAC includes a wide range of features designed for both **automated detection** and **staff investigation**.

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

PulseAC uses a modular check system, allowing individual detections to be configured and improved independently.

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

PulseAC organizes detections into separate checks, making it easier for server owners to configure and manage their anti-cheat.

| Category     | Checks                               |
| ------------ | ------------------------------------ |
| ⚔️ Combat    | KillAura, Reach, InvalidAttack       |
| 🏃 Movement  | Speed, Fly, NoFall, Phase, Jesus     |
| 🖱️ Clicking | CPS, AutoClicker, Click Patterns     |
| 👤 Player    | Invalid Movement, Abnormal Behaviour |

More checks will be added and improved as PulseAC continues development.

---

# 🚨 Violation System

PulseAC uses a **Violation Level (VL)** system to track suspicious behaviour.

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

Server owners can configure how violations are handled and what actions should occur at different thresholds.

---

# 👮 Staff System

PulseAC includes a collection of commands and permissions designed for server staff.

### `Pulse.staff`

Provides access to PulseAC staff functionality.

### `Pulse.alerts`

Allows staff members to receive real-time anti-cheat alerts.

### `Pulse.verbose`

Provides additional detection information for testing, debugging, and investigating suspicious behaviour.

---

# 👁️ Spectate System

PulseAC includes tools that allow staff members to investigate suspicious players directly in-game.

### `Pulse.spectate`

Allows authorized staff to spectate players under investigation.

### `Pulse.stopspectating`

Allows staff to stop spectating and return to their normal state.

---

# 👤 Player Profiles

### `Pulse.profile`

Provides staff with information about a player's PulseAC profile.

Profiles can include:

* Player name
* Violation levels
* Triggered checks
* Detection history
* Client information
* Current status
* Recent alerts

---

# 💻 Client Brand Detection

### `Pulse.clientbrand`

PulseAC can retrieve and display the Minecraft client brand reported by a player.

Client brand information can be useful when investigating suspicious behaviour alongside actual anti-cheat detections.

> **Client brand information alone should not be treated as proof that a player is cheating.**

---

# 🔄 Setback System

PulseAC supports configurable setbacks for checks where returning a player to a previous position is appropriate.

Setbacks can help prevent players from continuing abnormal movement after triggering a movement detection.

### `Pulse.nosetback`

Allows authorized users to bypass PulseAC setbacks.

This can be useful for:

* Staff
* Developers
* Testing
* Debugging
* Special server environments

---

# 🛡️ Bypass System

### `Pulse.bypass`

Allows authorized players to bypass configured PulseAC detections.

This can be useful for trusted:

* Staff members
* Developers
* Testers
* Server administrators

Bypass permissions should only be given to trusted users.

---

# 🔔 Staff Alerts

PulseAC provides real-time alerts to staff members with the appropriate permissions.

Example:

```text
PulseAC | Player: ExamplePlayer
Check: Speed
VL: 4
Detection: Abnormal Movement
Action: Setback
```

Alerts can be customized through the PulseAC configuration.

---

# 👁️ Investigation Tools

PulseAC gives staff multiple ways to investigate suspicious players instead of relying exclusively on automatic punishments.

Staff can use:

* Anti-cheat alerts
* Verbose information
* Player profiles
* Spectating
* Client brand information
* Violation levels
* Detection history

---

# ⚙️ Configuration

PulseAC is highly configurable.

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

---

# 🚀 Performance

PulseAC is designed with server performance in mind.

The goal is to continuously monitor player behaviour without creating unnecessary server overhead.

PulseAC focuses on:

* Efficient detection
* Modular checks
* Lightweight monitoring
* Configurable processing
* Scalable player tracking
* Minimal unnecessary processing

---

# 🧩 Modular Architecture

PulseAC uses a modular check system, making it easier to add, update, and maintain detections.

Each check can have its own:

* Detection system
* Configuration
* Violation handling
* Alert format
* Setback behaviour
* Punishment settings

---

# 🖥️ Compatibility

PulseAC is designed to support modern **Bukkit-based Minecraft server software**, with compatibility ranging from **Minecraft 1.8.8 through 1.21.x**.

| Server Software | Compatibility  |
| --------------- | -------------- |
| **Paper**       | 🌟 Recommended |
| **Purpur**      | 🌟 Recommended |
| **Pufferfish**  | 🌟 Recommended |
| **Folia**       | ✅ Supported    |
| **Spigot**      | ✅ Supported    |
| **CraftBukkit** | ✅ Supported    |

---

# ☕ Java Requirements

PulseAC requires a Java runtime appropriate for your Minecraft server version.

### Recommended

* **Java 17**
* **Java 21**

| Minecraft Version  | Recommended Java            |
| ------------------ | --------------------------- |
| **1.8.8 – 1.16.x** | Java 8 / compatible runtime |
| **1.17 – 1.20.4**  | Java 17                     |
| **1.20.5+**        | Java 21                     |
| **1.21.x**         | Java 21                     |

> The required Java version is primarily determined by the Minecraft server software and version you are running.

---

# 📦 Installation

1. Download the PulseAC `.jar`.
2. Place it inside your server's `plugins` folder.
3. Restart your server.
4. Open the generated PulseAC configuration.
5. Configure the checks you want enabled.
6. Configure staff permissions and alerts.
7. Test your configuration.
8. Enable automatic punishments after testing.

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

| Permission             | Purpose                             |
| ---------------------- | ----------------------------------- |
| `Pulse.staff`          | Access PulseAC staff functionality  |
| `Pulse.alerts`         | Receive anti-cheat alerts           |
| `Pulse.verbose`        | View detailed detection information |
| `Pulse.spectate`       | Spectate players                    |
| `Pulse.stopspectating` | Stop spectating                     |
| `Pulse.profile`        | View player profiles                |
| `Pulse.clientbrand`    | View client brand information       |
| `Pulse.nosetback`      | Bypass setbacks                     |
| `Pulse.bypass`         | Bypass configured checks            |

---

# 💬 Discord

## Coming Soon

The official **PulseAC Discord server** is currently **coming soon**.

The Discord will eventually provide a place for:

* 📢 PulseAC announcements
* 🆕 Update notifications
* 🐛 Bug reports
* 💡 Suggestions
* 💬 Community discussion
* 🛠️ Support
* 📚 Documentation
* 🔧 Development updates

**Official Discord — Coming Soon**

---

# 🔮 Future Development

PulseAC is actively designed for future expansion.

Potential future additions include:

* More advanced combat checks
* Improved movement analysis
* Additional inventory checks
* Better packet analysis
* Advanced reach analysis
* Improved AutoClicker detection
* Better false-positive prevention
* Expanded staff tools
* Web-based statistics
* Detection logs
* API support
* Developer API
* More configurable punishments
* Improved player profiles
* Additional investigation tools
* Official Discord community

---

# 🤝 Bug Reports & Contributions

If you discover a problem with PulseAC, please report it through the appropriate GitHub issue or development channel.

When reporting a bug, include as much information as possible:

* Minecraft version
* Server software
* PulseAC version
* Check that triggered
* Player behaviour
* Console output
* Configuration
* Steps to reproduce the issue

False positives should also be reported so detections can be investigated and improved.

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

---

# ⚡ PulseAC

**Detect fast. React faster.**

PulseAC combines automated detection with powerful staff investigation tools to help Minecraft servers monitor suspicious behaviour and maintain fair gameplay.

**Lightweight. Configurable. Modular. Built for Minecraft servers.**

**© PulseAC — All rights reserved.**
