# Changelog

All notable changes to **JP2 Création** will be documented in this file.  
This project adheres to [Semantic Versioning](https://semver.org/) and is inspired by [Keep a Changelog](https://keepachangelog.com/).

## [2.6.1] - 2025-09-07
### Added
- Display of **remote filename** next to `Dernière : vX.Y.Z` for remote plugins.
### Changed
- **JP2 Création** (remote) latest detection improved: parse versions from page text; guess common filenames (`jp2-creation-<ver>.zip`, etc.), HEAD‑check candidates.

## [2.6.0] - 2025-09-07
### Added
- **JP2 Gallery**: stronger latest detection from `https://jp2.fr/jp2_plugins/jp2-gallery/` (parse versions in text, guess filenames, HEAD checks).
- UI shows `Dernière : vX.Y.Z` for remote plugins (JP2 Gallery, JP2 Création).

## [2.5.1] - 2025-09-07
### Added
- **Override constants** for remote sources:
  - `JP2C_JP2CREATION_URL` (JP2 Création)
  - `JP2C_JP2GALLERY_URL` (JP2 Gallery)

## [2.5.0] - 2025-09-07
### Added
- Display **latest remote version** in status column.
### Changed
- Remote detection: HEAD probe on non‑`.zip` links (checks `Content-Type` / `Content-Disposition`).

## [2.4.0] - 2025-09-07
### Added
- Added **JP2 Création** (remote) to bundle (auto latest from page).
### Removed
- **Debug** tab and WP_DEBUG/WP_DEBUG_LOG toggles (as requested).

## [2.3.0] - 2025-09-07
### Added
- Added **JP2 Gallery** (remote) with auto latest detection from page.
