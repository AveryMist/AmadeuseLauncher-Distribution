# Amadeuse Launcher Distribution

This repository contains the distribution files for Amadeuse Launcher, providing two carefully curated Minecraft modpacks.

## 🎮 Available Modpacks

### 1. VERSION 1.21.4 SEMI-VANILLA (NEOFORGE)
- **Latest Minecraft 1.21.4** with NeoForge mod loader
- **Includes:**
  - **Essential** - Play with friends, voice chat, and cosmetics
  - **Controllable** - Full gamepad/controller support
- **Perfect for** playing with friends while enjoying the latest Minecraft features

### 2. VERSION 1.12.2 HYPIXEL (FORGE)
- **Optimized for Hypixel server** gameplay with Forge
- **Includes:**
  - **Essential** - Play with friends and voice chat
  - **Controllable** - Full gamepad/controller support
  - **BetterFps** - Performance optimizations
  - **Damage Indicators** - PvP enhancements
  - **Mo' Bends** - Smooth animations
  - **Dynamic Surroundings** - Immersive audio
- **Perfect for** Hypixel minigames with friends and controller support

## 📁 Repository Structure

```
github_distribution/
├── distribution.json          # Main distribution configuration
├── rss.xml                   # News feed
├── servers/                  # Server-specific files
│   ├── minecraft-1.21.4-neoforge/     # NeoForge with Essential + Controllable
│   └── minecraft-1.12.2-hypixel/      # Forge with Hypixel optimization mods
└── repo/                     # Mod and library files
    ├── lib/                  # Libraries and mod loaders
    │   ├── net/minecraftforge/forge/   # Forge 1.12.2
    │   └── net/neoforged/neoforge/     # NeoForge 1.21.4
    └── versions/             # Version manifests
        ├── 1.12.2-forge-14.23.5.2859/
        └── 1.21.4-neoforge-21.4.18/
```

## 🔗 Usage

To use this distribution with Amadeuse Launcher, update the distribution URL in the launcher to:
```
https://raw.githubusercontent.com/AveryMist/AmadeuseLauncher-Distribution/main/distribution.json
```

## 🛠️ Adding Mods

To add new mods to any modpack:

1. Upload the mod file to the appropriate `servers/{modpack}/mods/` directory
2. Calculate the MD5 hash of the file
3. Update the `distribution.json` with the new mod entry
4. Commit and push changes

## 📞 Support

- **Discord:** https://discord.gg/GEZCQwczMY
- **GitHub Issues:** https://github.com/AveryMist/AmadeuseLauncher/issues

## 📄 License

This distribution is provided for use with Amadeuse Launcher. Individual mods retain their respective licenses.
