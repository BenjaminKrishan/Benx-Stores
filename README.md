# 🏪 BenX Stores – Modern Business & Mission Ecosystem

> **Experience the next generation of FiveM store ownership.** BenX Stores has been completely modernized with a premium GTA-style Scaleform system, advanced mission HUDs, and hardened security. Built for **Qbox** and the **OX Stack**, it offers unparalleled immersion and stability.

<p align="center">
  <img src="https://img.shields.io/badge/Framework-QBox-orange?style=for-the-badge" alt="Framework">
  <img src="https://img.shields.io/badge/Inventory-Ox--Inventory-blue?style=for-the-badge" alt="Inventory">
  <img src="https://img.shields.io/badge/UI-Ox--Lib-purple?style=for-the-badge" alt="UI">
  <img src="https://img.shields.io/badge/Version-1.0-red?style=for-the-badge" alt="Version">
</p>

---

## ✨ Modernized Features

### 🎭 Premium Scaleform Notifications
Forget generic popups. BenX Stores uses **GTA-style Midsized Scaleforms** for all major business events:
- **Financials**: Deposit/Withdrawal confirmations with real-time balance updates.
- **Management**: Visual feedback for price edits, stock additions, and mission creation.
- **Real Estate**: Immersive "Property Purchased/Sold" celebrations.

### 🚚 Enhanced Mission Ecosystem
Missions are now more informative and secure:
- **Detailed Navigation HUD**: Real-time tracking showing **Destination**, **Item Name**, **Quantity**, and **Estimated Reward**.
- **Model-Based Restrictions**: No more generic vehicle classes. Owners can specify exact vehicle models (e.g., `benson`, `mule`) required for deliveries.
- **Race-Condition Protection**: Atomic mission claiming logic ensures two players can never claim the same job simultaneously.
- **Automatic Cleanup**: Blips, HUDs, and GPS routes are automatically managed on disconnect, resource stop, or mission completion.

### 🛡️ Core Stability & Optimization
- **Zero Legacy Code**: All deprecated compatibility layers have been removed for a lightweight, performant script.
- **Centralized Localization**: All player-facing text is now in `Config.Messages` for instant translation.
- **Database Integrity**: Uses `oxmysql` with careful synchronization between server memory and persistent storage.

---

## 🚀 Installation

1. **Prerequisites**: Ensure you have `qbx_core`, `ox_inventory`, `ox_lib`, and `oxmysql` installed and running.
2. **Database**: Import the `sql.sql` file provided in the resource folder.
3. **Files**: Drag and drop `benx_stores` into your `[resources]` directory.
4. **Configuration**: Review `config.lua` to set your desired stores, items, and vehicle restrictions.
5. **Start**: Add `ensure benx_stores` to your `server.cfg`.

---

## 📋 Commands & Controls

| Action | Control/Command |
|--------|-----------------|
| **Browse Shop** | Interact via **Target** (ox_target) |
| **Manage Business** | Interact via **Target** (Office Area) |
| **Mission Board** | Interact via **Target** (Shop Counter) |
| **Cancel Mission** | `/cancelmission` (Available via command or UI) |

---

## ⚙️ Key Configuration (`config.lua`)

| Key | Example | Description |
|-----|---------|-------------|
| `Config.AllowedVehicleTypes` | `{'benson', 'mule'}` | List of specific vehicle models allowed for missions. |
| `Config.MissionCooldown` | `300` | Seconds a player must wait between missions. |
| `Config.CancelPenalty` | `10` | Percentage of reward deducted if a mission is cancelled. |
| `Config.Scaleforms` | *(Object)* | Fully customizable visual/audio settings for all notifications. |

---

<p align="center">
  <strong>📦 Premium FiveM Resources by BenX Development</strong><br>
  <a href="https://benx.tebex.io/">
    <img src="https://img.shields.io/badge/Visit%20Tebex%20Store-blue?style=for-the-badge&logo=tebex" alt="Tebex Store">
  </a>
</p>

*© 2026 Benjamin Krishan - BenX Development. Modernized for performance, immersion, and stability.*
