# JP2 Création

**Plugin WordPress** qui facilite l’installation et la maintenance d’un bundle d’extensions/thèmes pour sites JP2 Création, et permet d’injecter du code dans `<head>` et en pied de page.

> FR 🇫🇷 — English version below ⬇️

## ✨ Fonctionnalités
- **Gestionnaire de bundle** (*Extensions → JP2 Création → Plugins & Thème*) :
  - Plugins wp.org : **Elementor**, **MainWP Child**, **Royal Elementor Addons**, **Widgets for Google Reviews (Trustindex)**, **Yoast SEO**.
  - Plugins distants (« remote ») : **JP2 Gallery**, **JP2 Création** — la **dernière version** est détectée automatiquement depuis leur page; affichage `Dernière : vX.Y.Z` + nom du fichier.
  - **PRO Elements** : installation/mise à jour via **auto‑détection** (site/GitHub) ou **URL manuelle** (.zip), avec écrasement du dossier existant.
  - Thème : **Hello Elementor** (wp.org).
- **Actions individuelles** : Installer / Activer / Désactiver / Mettre à jour (aucune action “Tout installer/MAJ”).  
- **Injection de code** : onglet *Code head & footer* pour coller du code libre (métas, pixels, scripts).
- **Détection robuste des .zip** : scraping des liens, HEAD check `Content-Type`/`Content-Disposition`, heuristiques de nommage pour JP2 Gallery / JP2 Création.
- **Écrasement sécurisé** (overwrite) lors des installations depuis une URL : plus d’erreur « le dossier existe déjà ».
- **Cache** : résultat des détections distant : **6 h** (transients).

## 🔧 Overrides & options
- **PRO Elements** (champ dans l’admin) ou constante :
  ```php
  define('JP2C_PRO_URL', 'https://…/pro-elements.zip');
  ```
- **Forcer les sources “remote”** :
  ```php
  // JP2 Création (plugin distant)
  define('JP2C_JP2CREATION_URL', 'https://jp2.fr/jp2_plugins/jp2creation/jp2-creation-2.5.0.zip');
  // JP2 Gallery
  define('JP2C_JP2GALLERY_URL', 'https://jp2.fr/jp2_plugins/jp2-gallery/jp2-gallery-1.4.2.zip');
  ```
> Placez ces constantes dans `wp-config.php` (au‑dessus de « That’s all, stop editing! »).

## 🧭 Navigation
- **Extensions → JP2 Création**  
  - **Plugins & Thème** : gestion unitaire des items (statut, version locale, dernière distante, actions).  
  - **Code head & footer** : activez/désactivez et collez vos snippets.

## ✅ Prérequis
- WordPress **6.x** recommandé
- PHP **7.4+** (8.0/8.1/8.2 conseillés)
- Rôle capable de `install_plugins` (administrateur)

## 🚀 Installation
1. Téléchargez la **release** `.zip` depuis GitHub.
2. *Extensions → Ajouter → Téléverser une extension* → sélectionnez le zip → **Activer**.
3. Allez dans **Extensions → JP2 Création** pour gérer le bundle.

## 🛡️ Sécurité & limites
- Les installations depuis URL supposent des **sources publiques de confiance** (wp.org / GitHub / domaine JP2).
- La détection distante peut dépendre du **contenu de la page** et des **headers HTTP** ; si nécessaire, utilisez les **constantes d’override** ci‑dessus.

## 📝 Licence
MIT (voir `LICENSE`).

---

## JP2 Création (EN)

**WordPress plugin** to quickly install & maintain a curated stack of plugins/themes for JP2 Création sites, plus inline code injection for `<head>` and footer.

### Features
- **Bundle manager** (*Plugins → JP2 Création → Plugins & Thème*):
  - wp.org plugins: **Elementor**, **MainWP Child**, **Royal Elementor Addons**, **Widgets for Google Reviews (Trustindex)**, **Yoast SEO**.
  - Remote plugins: **JP2 Gallery**, **JP2 Création** — **latest version** auto‑detected from their landing pages; shows `Latest: vX.Y.Z` + filename.
  - **PRO Elements**: auto‑discover download link (site/GitHub) or use a **manual .zip URL**, with destination overwrite.
  - Theme: **Hello Elementor**.
- **Per‑item actions** only (no “install all/update all”).  
- **Head & footer code** tab to inject custom snippets.
- **Robust .zip detection** (link scraping + HEAD checks + JP2 heuristics).
- **Overwrite on install** from URL (avoids “destination folder already exists”).
- **6h cache** for remote lookups (transients).

### Overrides & options
```php
define('JP2C_PRO_URL', 'https://…/pro-elements.zip');
define('JP2C_JP2CREATION_URL', 'https://jp2.fr/jp2_plugins/jp2creation/jp2-creation-2.5.0.zip');
define('JP2C_JP2GALLERY_URL', 'https://jp2.fr/jp2_plugins/jp2-gallery/jp2-gallery-1.4.2.zip');
```

### Requirements
- WordPress **6.x**
- PHP **7.4+**
- User with `install_plugins` capability

### Install
Upload the `.zip` in *Plugins → Add New → Upload*, then use **Plugins → JP2 Création** to manage the bundle.

### License
MIT.
