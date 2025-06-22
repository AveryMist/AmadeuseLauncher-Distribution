# Système de Gestion des Mods - Amadeuse Launcher

## Vue d'ensemble

Ce système utilise des **IDs uniques** pour chaque mod afin de permettre au launcher de gérer automatiquement :
- ✅ **Ajout de nouveaux mods**
- ✅ **Mise à jour des mods existants**
- ✅ **Suppression des mods retirés**
- ✅ **Séparation par version/loader**

## Structure des IDs

Format : `{mod-name}-{loader}-{minecraft-version}`

### Exemples :
- `essential-forge-1.12.2` → Essential pour Forge 1.12.2
- `essential-neoforge-1.21.4` → Essential pour NeoForge 1.21.4
- `controllable-forge-1.12.2` → Controllable pour Forge 1.12.2
- `controllable-neoforge-1.21.4` → Controllable pour NeoForge 1.21.4

## Fichiers de configuration

### 1. `mod-downloads.json`
Fichier de référence contenant tous les mods avec leurs métadonnées complètes :
- IDs uniques
- Versions
- URLs de téléchargement
- Informations de compatibilité
- Dépendances

### 2. `distribution.json`
Configuration principale du launcher utilisant les IDs du fichier `mod-downloads.json`

## Comment ajouter un nouveau mod

### 1. Ajouter dans `mod-downloads.json` :
```json
"nouveau-mod-forge-1.12.2": {
  "id": "nouveau-mod-forge-1.12.2",
  "name": "Nouveau Mod",
  "version": "1.0.0",
  "filename": "nouveau-mod-1.0.0.jar",
  "url": "https://www.curseforge.com/minecraft/mc-mods/nouveau-mod/download/123456",
  "curseforge_project_id": "nouveau-mod",
  "curseforge_file_id": "123456",
  "required": false,
  "client_side": "required",
  "server_side": "optional"
}
```

### 2. Ajouter dans `distribution.json` :
```json
{
  "id": "nouveau-mod-forge-1.12.2",
  "name": "Nouveau Mod",
  "type": "ForgeMod",
  "artifact": {
    "size": 1000000,
    "url": "https://www.curseforge.com/minecraft/mc-mods/nouveau-mod/download/123456",
    "MD5": "HASH_MD5_DU_FICHIER"
  }
}
```

## Comment supprimer un mod

1. **Retirer l'entrée** du `distribution.json`
2. **Optionnel** : Retirer aussi du `mod-downloads.json` (pour nettoyage)
3. Le launcher détectera automatiquement que le mod n'est plus requis et le supprimera

## Comment mettre à jour un mod

1. **Modifier l'URL** et le `curseforge_file_id` dans `mod-downloads.json`
2. **Modifier l'URL** et le `MD5` dans `distribution.json`
3. Le launcher détectera automatiquement la différence de hash et téléchargera la nouvelle version

## Avantages de ce système

### 🎯 **Gestion automatique**
- Le launcher compare les IDs locaux avec ceux du serveur
- Détection automatique des ajouts/suppressions/mises à jour

### 🔄 **Séparation par version**
- Mods 1.12.2 Forge séparés des mods 1.21.4 NeoForge
- Pas de conflit entre les versions

### 📦 **Sources multiples**
- CurseForge pour les gros mods (pas de limite de taille)
- GitHub pour les petits fichiers et configs
- Facilement extensible à d'autres sources

### 🛡️ **Sécurité**
- Hash MD5 pour vérifier l'intégrité des fichiers
- URLs directes vers les sources officielles

## Exemple de workflow

### Ajouter Essential à une nouvelle version :
1. ID : `essential-fabric-1.20.1`
2. URL CurseForge pour Fabric 1.20.1
3. Ajouter dans les deux fichiers JSON
4. Push → Le launcher détecte et télécharge automatiquement

### Retirer un mod obsolète :
1. Supprimer l'entrée du `distribution.json`
2. Push → Le launcher détecte et supprime le mod local

Cette approche garantit que chaque utilisateur a exactement les mods requis pour sa version, sans conflit ni erreur de téléchargement.
