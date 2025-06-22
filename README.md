# 🚀 Amadeuse Launcher Distribution

<div align="center">

![Amadeuse Launcher](https://img.shields.io/badge/Amadeuse-Launcher-blue?style=for-the-badge)
![Minecraft](https://img.shields.io/badge/Minecraft-1.12.2%20%7C%201.21.4-green?style=for-the-badge)
![Modpacks](https://img.shields.io/badge/Modpacks-2-orange?style=for-the-badge)

**Official distribution repository for Amadeuse Launcher**
*Two carefully curated Minecraft modpacks for the ultimate gaming experience*

</div>

---

## 🎮 **Featured Modpacks**

<table>
<tr>
<td width="50%">

### 🌟 **VERSION 1.21.4 SEMI-VANILLA (NEOFORGE)**
*Latest Minecraft with enhanced multiplayer*

**🔧 Mod Loader:** NeoForge 21.4.140
**🎯 Target:** Latest Minecraft experience with friends

**📦 Included Mods:**
- 👥 **Essential** - Voice chat, cosmetics, friends system
- 🎮 **Controllable** - Full gamepad support

**✨ Perfect for:**
- Playing with friends
- Latest Minecraft features
- Cross-platform gaming
- Voice communication

</td>
<td width="50%">

### ⚔️ **VERSION 1.12.2 HYPIXEL (FORGE)**
*Optimized for competitive Hypixel gameplay*

**🔧 Mod Loader:** Forge 14.23.5.2860
**🎯 Target:** Hypixel server optimization

**📦 Included Mods:**
- 👥 **Essential** - Friends and voice chat
- 🎮 **Controllable** - Controller support
- ⚡ **BetterFps** - Performance boost
- 💥 **Damage Indicators** - PvP advantage
- 🎭 **Mo' Bends** - Smooth animations
- 🎵 **Dynamic Surroundings** - Immersive audio
- 📚 **OreLib** - Required library

**✨ Perfect for:**
- Hypixel minigames
- PvP combat
- Controller gaming
- Performance optimization

</td>
</tr>
</table>

---

## 🔧 **Advanced Mod Management System**

Amadeuse Launcher utilise un **système d'ID unique** pour chaque mod, permettant une gestion automatique intelligente :

### ✨ **Fonctionnalités Automatiques**
- 🆕 **Auto-détection des nouveaux mods** - Téléchargement automatique
- 🔄 **Mise à jour intelligente** - Détection des nouvelles versions
- 🗑️ **Suppression automatique** - Nettoyage des mods retirés
- 🎯 **Séparation par version** - Pas de conflit entre Forge/NeoForge

### 🏷️ **Système d'ID Unique**
Chaque mod a un ID spécifique : `{mod-name}-{loader}-{minecraft-version}`

**Exemples :**
- `essential-forge-1.12.2` → Essential pour Forge 1.12.2
- `essential-neoforge-1.21.4` → Essential pour NeoForge 1.21.4
- `controllable-forge-1.12.2` → Controllable pour Forge 1.12.2

### 📦 **Sources de Téléchargement**
- 🌐 **CurseForge** - Mods principaux (pas de limite de taille)
- 📁 **GitHub** - Configurations et petits fichiers
- 🔒 **Vérification MD5** - Intégrité garantie

> 📖 **Documentation complète :** Voir [MOD_MANAGEMENT.md](MOD_MANAGEMENT.md) pour les détails techniques

---

## 🏗️ **Technical Overview**

<details>
<summary><b>📁 Repository Structure</b></summary>

```
AmadeuseLauncher-Distribution/
├── 📄 distribution.json          # Main distribution configuration
├── 🔧 mod-downloads.json         # Mod management database with unique IDs
├── 📖 MOD_MANAGEMENT.md          # Technical documentation for mod system
├── 📰 rss.xml                   # News feed for launcher
├── 📚 README.md                 # This documentation
├── 🖥️ servers/                  # Modpack configurations
│   ├── minecraft-1.21.4-neoforge/     # NeoForge modpack
│   │   ├── mods/                       # NeoForge mods
│   │   └── ICON.png                    # Modpack icon
│   └── minecraft-1.12.2-hypixel/      # Forge modpack
│       ├── mods/                       # Forge mods
│       ├── overrides/config/           # Pre-configured settings
│       └── ICON.png                    # Modpack icon
└── 📦 repo/                     # Mod loaders and libraries
    ├── lib/                            # Mod loader files
    │   ├── net/minecraftforge/forge/   # Forge 1.12.2
    │   └── net/neoforged/neoforge/     # NeoForge 1.21.4
    └── versions/                       # Version manifests
        ├── 1.12.2-forge-14.23.5.2860/
        └── 1.21.4-neoforge-21.4.140/
```

</details>

<details>
<summary><b>⚙️ System Requirements</b></summary>

### Minimum Requirements
- **Java:** 8+ (1.12.2) / 21+ (1.21.4)
- **RAM:** 4GB allocated to Minecraft
- **Storage:** 2GB free space
- **Internet:** Stable connection for downloads

### Recommended Requirements
- **Java:** Latest LTS version
- **RAM:** 6-8GB allocated to Minecraft
- **Storage:** 5GB free space
- **Controller:** Xbox/PlayStation/Generic USB (optional)

</details>

---

## 🚀 **Getting Started**

### 📥 **Download Amadeuse Launcher**
1. Visit the [Amadeuse Launcher releases](https://github.com/AveryMist/AmadeuseLauncher/releases)
2. Download the latest version for your operating system
3. Install and launch the application
4. The modpacks will be automatically available!

### 🎮 **Choose Your Adventure**
- **New to Minecraft?** → Try **1.21.4 Semi-Vanilla** for the latest features
- **Hypixel Player?** → Choose **1.12.2 Hypixel** for optimized gameplay
- **Controller User?** → Both modpacks support full gamepad controls!

---

## 🤝 **Community & Support**

<div align="center">

[![Discord](https://img.shields.io/discord/YOUR_DISCORD_ID?color=7289da&label=Discord&logo=discord&logoColor=white&style=for-the-badge)](https://discord.gg/GEZCQwczMY)
[![GitHub Issues](https://img.shields.io/github/issues/AveryMist/AmadeuseLauncher?style=for-the-badge&logo=github)](https://github.com/AveryMist/AmadeuseLauncher/issues)

**Join our community for support, updates, and gaming together!**

</div>

### � **Get Help**
- 🆘 **Technical Issues:** [GitHub Issues](https://github.com/AveryMist/AmadeuseLauncher/issues)
- 💭 **General Chat:** [Discord Server](https://discord.gg/GEZCQwczMY)
- 📖 **Documentation:** Check the launcher's built-in help

### 🔄 **Stay Updated**
- ⭐ **Star this repository** to get notified of updates
- 📢 **Follow us on Discord** for announcements
- 🔔 **Enable GitHub notifications** for release updates

---

## 📄 **License & Credits**

<div align="center">

**Made with ❤️ by the Amadeuse Team**

*This distribution is provided for use with Amadeuse Launcher.*
*Individual mods retain their respective licenses and credits to their creators.*

[![GitHub](https://img.shields.io/badge/GitHub-AveryMist-black?style=for-the-badge&logo=github)](https://github.com/AveryMist)

</div>
