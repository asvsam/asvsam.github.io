---
layout: default
title: " - CoreConfig"
parent: Benutzer-Handbuch
permalink: /asvsam/config_ui_konfiguration/CoreConfig
nav_order: 130
---

# UI - Konfiguration - CoreConfig


## ÜBERSICHT - Basiskonfiguration (CORE_CONFIG)

Konfiguration des Regelsets zur Erstellung von eineindeutigen Benutzernamen, auf Basis der jeweiligen Vor- und Nachnamen der Schüler.

| <!-- -->               | <!-- -->                                                                                                                                                                                                                                                                                                                   |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Konfigurationsort**  | GUI: Entitäten -> Konfiguration                                                                                                                                                                                                                                                                                            |
| **Konfig-Typ**         | CORE_CONFIG                                                                                                                                                                                                                                                                                                                |
| **Mögliche Schlüssel** | - CORE_BENUTZERNAME_VORNAME_MIN_LEN<br/>- CORE_BENUTZERNAME_VORNAME_MAX_LEN<br/>- CORE_BENUTZERNAME_VORNAME_CUTOFF_CHARS<br/>- CORE_BENUTZERNAME_NACHNAME_MIN_LEN<br/>- CORE_BENUTZERNAME_NACHNAME_MAX_LEN<br/>- CORE_BENUTZERNAME_NACHNAME_CUTOFF_CHARS<br/>- CORE_BENUTZERNAME_MAX_LEN<br/>- CORE_BENUTZERNAME_SEPARATOR |

Im Folgenden wird eine Detailbeschreibung der möglichen Schlüssel aufgelistet.

## WERT - CORE_BENUTZERNAME_VORNAME_MIN_LEN

| <!-- -->                   | <!-- -->                                                                                 |
|----------------------------|------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | CORE_CONFIG / CORE_BENUTZERNAME_VORNAME_MIN_LEN                                          |
| **Standardwert**           | 3                                                                                        |
| **Datentyp**               | Integer (>1)                                                                             |
| **Wertebereich**           | Ganzzahl - Minimale Anzahl an Zeichen des Vornamens zur Verwendung in dem Benutzernamen. |

## WERT - CORE_BENUTZERNAME_VORNAME_MAX

| <!-- -->                   | <!-- -->                                                                                 |
|----------------------------|------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | CORE_CONFIG / CORE_BENUTZERNAME_VORNAME_MAX                                              |
| **Standardwert**           | 8                                                                                        |
| **Datentyp**               | Integer (>1)                                                                             |
| **Wertebereich**           | Ganzzahl - Maximale Anzahl an Zeichen des Vornamens zur Verwendung in dem Benutzernamen. |

## WERT - CORE_BENUTZERNAME_VORNAME_CUTOFF_CHARS

| <!-- -->                   | <!-- -->                                                                                                                                       |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | CORE_CONFIG / CORE_BENUTZERNAME_VORNAME_CUTOFF_CHARS                                                                                           |
| **Standardwert**           | -                                                                                                                                              |
| **Datentyp**               | Zeichen                                                                                                                                        |
| **Wertebereich**           | Verwendetes Trennzeichen das einschließlich und mit dem Textteil rechts davon vom Vornamen abgeschnitten wird, zur Bildung der Benutzernamens. |

## WERT - CORE_BENUTZERNAME_NACHNAME_MIN_LEN

| <!-- -->                   | <!-- -->                                                                                  |
|----------------------------|-------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | CORE_CONFIG / CORE_BENUTZERNAME_NACHNAME_MIN_LEN                                          |
| **Standardwert**           | 3                                                                                         |
| **Datentyp**               | Integer (>2)                                                                              |
| **Wertebereich**           | Ganzzahl - Minimale Anzahl an Zeichen des Nachnamens zur Verwendung in dem Benutzernamen. |

## WERT - CORE_BENUTZERNAME_NACHNAME_MAX_LEN

| <!-- -->                   | <!-- -->                                                                                  |
|----------------------------|-------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | CORE_CONFIG / CORE_BENUTZERNAME_NACHNAME_MAX_LEN                                          |
| **Standardwert**           | 12                                                                                        |
| **Datentyp**               | Integer (>5)                                                                              |
| **Wertebereich**           | Ganzzahl - Maximale Anzahl an Zeichen des Nachnamens zur Verwendung in dem Benutzernamen. |

## WERT - CORE_BENUTZERNAME_NACHNAME_CUTOFF_CHARS

| <!-- -->                   | <!-- -->                                                                                                                                        |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | CORE_CONFIG / CORE_BENUTZERNAME_NACHNAME_CUTOFF_CHARS                                                                                           |
| **Standardwert**           | -                                                                                                                                               |
| **Datentyp**               | Zeichen                                                                                                                                         |
| **Wertebereich**           | Verwendetes Trennzeichen das einschließlich und mit dem Textteil rechts davon vom Nachnamen abgeschnitten wird, zur Bildung des Benutzernamens. |

## WERT - CORE_BENUTZERNAME_MAX_LEN

| <!-- -->                   | <!-- -->                                                 |
|----------------------------|----------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | CORE_CONFIG / CORE_BENUTZERNAME_MAX_LEN                  |
| **Standardwert**           | 12                                                       |
| **Datentyp**               | Integer (>5)                                             |
| **Wertebereich**           | Maximale Anzahl an Zeichen des erzeugtem Benutzernamens. |

## WERT - CORE_BENUTZERNAME_SEPARATOR

| <!-- -->                   | <!-- -->                                                                       |
|----------------------------|--------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | CORE_CONFIG / CORE_BENUTZERNAME_SEPARATOR                                      |
| **Standardwert**           | .                                                                              |
| **Datentyp**               | Zeichen                                                                        |
| **Wertebereich**           | Verwendetes Trennzeichen im Benutzernamen zur Trennung von Vor- und Nachnamen. |

## WERT - CORE_ADMINISTRATOR_EMAIL

| <!-- -->                   | <!-- -->                                                                                                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | CORE_CONFIG / CORE_ADMINISTRATOR_EMAIL                                                                                                                                   |
| **Standardwert**           | admin@localhost                                                                                                                                                          |
| **Datentyp**               | String (Gültige Emailadresse)                                                                                                                                            |
| **Wertebereich**           | Emailadresse des Administrators oder Systemverantwortlichen. Diese Emailadresse wird von System verwendet, um über ungewöhnliche Systemzustände und Fehler zu berichten. |

