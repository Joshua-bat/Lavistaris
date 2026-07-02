<p align="center">
  <img src="icon.png" width="140" alt="Lavistaris logo">
</p>

# Lavistaris

Ein dunkel-lila / mystisches Theme für Home Assistant mit Light- und Dark-Mode, eigenem Hintergrundbild und [card_mod](https://github.com/thomasloven/lovelace-card-mod) Unterstützung für transparente Karten.

![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg?style=for-the-badge)

## Vorschau

| Light | Dark |
|---|---|
| ![Lavistaris Light](images/preview-light.png) | ![Lavistaris Dark](images/preview-dark.png) |
| `#8E6BB8` / `#EBD6F5` | `#4B2A6A` / `#2E1A3F` |

## Voraussetzungen

- [HACS](https://hacs.xyz/) installiert
- Das Frontend-Modul [card_mod](https://github.com/thomasloven/lovelace-card-mod) installiert und als Ressource eingebunden (für die transparenten Karten-Hintergründe)
- Zwei Hintergrundbilder unter `/config/www/`:
  - `Lavistaris_light.png`
  - `Lavistaris_dark.png`

  (werden dann über `/local/...` referenziert)

## Installation

### Über HACS (empfohlen)

1. HACS → drei Punkte oben rechts → **Benutzerdefinierte Repositories**
2. Repository-URL eintragen: `https://github.com/DEIN-USERNAME/lavistaris-theme`
3. Kategorie: **Theme**
4. **Hinzufügen** klicken, danach das Theme in der HACS-Übersicht installieren
5. Home Assistant neu starten oder unter **Entwicklerwerkzeuge → YAML → Themes neu laden**
6. Unter **Einstellungen → Personalisierung → Theme** `Lavistaris` auswählen

### Manuell

1. Ordner `themes/Lavistaris.yaml` nach `/config/themes/Lavistaris.yaml` kopieren
2. In der `configuration.yaml` sicherstellen, dass Themes aktiviert sind:
   ```yaml
   frontend:
     themes: !include_dir_merge_named themes
   ```
3. Home Assistant neu starten
4. Theme unter **Einstellungen → Personalisierung** auswählen

## Enthaltene Variablen

Das Theme setzt u. a. `primary-color`, `accent-color`, `sidebar-*`, `app-header-*` sowie ein eigenes `lovelace-background` pro Modus. Über `card-mod-card` wird zusätzlich der Hintergrund jeder `ha-card` leicht transparent eingefärbt.

## Lizenz

MIT – siehe [LICENSE](LICENSE)
