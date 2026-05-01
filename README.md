# 🏪 BenX Stores System - Advanced Management

> *The ultimate store ownership and management system for QBox and QB-Core servers.*

<p align="center">
  <img src="https://img.shields.io/badge/Framework-QBox--QBCORE-orange?style=for-the-badge" alt="Framework">
  <img src="https://img.shields.io/badge/Inventory-Ox--Inventory-blue?style=for-the-badge" alt="Inventory">
  <img src="https://img.shields.io/badge/Version-1.2.0-green?style=for-the-badge" alt="Version">
</p>

---

### 🛒 Elevate Your Server Economy
**BenX Stores** is a high-performance, player-driven economy system that allows users to buy, manage, and optimize their own businesses. From stock delivery missions to real-time price customization, this script provides total control to business owners while ensuring server stability with hardened security.

---

## 🚀 Key Features

### 🏢 Comprehensive Management
Owners can manage their stores via a sleek **ox_lib** interface.
- **Real-time Balance**: Add or withdraw funds from the business account.
- **Stock Control**: Add items from your inventory directly to the store shelves.
- **Price Customization**: Adjust sell prices on the fly without needing a server restart.
- **Category Organization**: Group items into custom categories (Tools, Weapons, Food, etc.) for a better customer experience.

### 🚚 Dynamic Delivery Missions
Keep the shelves full with a built-in mission system.
- **Stock Requests**: Owners create missions with specific quantities and rewards.
- **Driver Bonuses**: Set an **Extra Delivery Fee** to attract players to fulfill your orders.
- **Configurable Limits**: Global and per-item limits on `min_request` and `max_request`.

### 🛡️ Hardened Security & Optimization
- **Race-Condition Protection**: Mission claiming is protected by server-side mutex logic.
- **Anti-Exploit**: Time-based validation prevents instant mission completion hacks.
- **Proximity Sync**: Database updates are broadcast only to nearby players to reduce network overhead.
- **Safe Loading**: Coordinate decoding is protected by `pcall` to prevent server crashes on malformed data.

---

## 🚀 Installation

1. **Prerequisites**: Ensure you have `qb-core`, `ox_inventory`, and `ox_lib` installed.
2. **Database**: Import the provided `sql.sql` file into your database.
3. **Download and Extract**: Place the `benx_stores` folder into your `resources` directory.
4. **Add to Server Config**:
   ```bash
   ensure benx_stores
   ```

---

## 📋 Commands

| Command | Description |
|---------|-------------|
| `/cancelmission` | Forces the cancellation of your current active delivery mission. |

---

## ⚙️ Configuration (`config.lua`)

| Key | Default | Description |
|-----|---------|-------------|
| `Config.DefaultMaxRequest` | `100` | Max items allowed per delivery request. |
| `Config.DefaultMinRequest` | `10` | Min items allowed per delivery request. |
| `Config.DefaultMinExtraFee` | `500` | Lowest bonus allowed for drivers. |
| `Config.DefaultMaxExtraFee` | `5000` | Highest bonus allowed for drivers. |
| `Config.VehicleCheck` | `true` | Requires a van/truck for delivery missions. |

---

<p align="center">
  <strong>📦 Need support or custom scripts?</strong><br>
  <a href="https://benx.tebex.io/category/scripts">
    <img src="https://img.shields.io/badge/Buy%20Now%20on%20Tebex-%249.49-important?style=for-the-badge&logo=tebex" alt="Buy on Tebex">
  </a>
</p>

*© 2026 Benjamin Krishan - BenX Development. All rights reserved.*
