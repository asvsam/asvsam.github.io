---
layout: default
title: UI - Konfiguration - Übersicht
parent: Benutzer-Handbuch
permalink: /asvsam/config_ui_konfiguration
nav_order: 100
---

# ASV-SAM UI - Konfiguration

## Konfiguration

Die Einträge in der Tabelle Konfiguration benötigen verschiedenen Attribute, welche im Folgenden beschrieben werden.

Das Attribut Konfigurations-Typen, bestimmt den Teil der Anwendung auf den sich der Konfigurationseintrag bezieht. Möglich Werte sind:

id;konfig\_typ;schluessel;wert

## ASV-Importer-Konfiguration (ASV_IMPORT_CONFIG)

Konfiguration des ASV-Importers für die Übernahme der Daten aus ASV (Via CSV, XML oder ASB-Datenbank).

### Übersicht - ASV_IMPORT_CONFIG

| ASV_IMPORT_CONFIG |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Konfigurationsort | GUI: Entitäten -> Konfiguration                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Konfig-Typ        | ASV_IMPORT_CONFIG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Mögliche Schlüssel | - ASV_IMPORT_GEBURTSTAG_DATEFORMAT<br/>- ASV_IMPORT_EINTRITTSDATUM_DATEFORMAT<br/>- ASV_IMPORT_AUSTRITTSDATUM_DATEFORMAT<br/>- ASV_IMPORT_EMAIL_REGEX<br/>- ASV_IMPORT_GESCHLECHT_REGEX<br/>- ASV_IMPORT_KLASSENBEZEICHNUNG_REGEX<br/>- ASV_IMPORT_SCHUELERID_REGEX<br/>- ASV_IMPORT_SCHUELERNR_REGEX<br/>- ASV_IMPORT_VORNAME_REGEX<br/>- ASV_IMPORT_NACHNAME_REGEX<br/>- ASV_IMPORT_KLASSENBEZEICHNUNG_MANDATORY<br/>- ASV_IMPORT_SCHUELERID_MANDATORY<br/>- ASV_IMPORT_SCHUELERNR_MANDATORY<br/>- ASV_IMPORT_VORNAME_MANDATORY<br/>- ASV_IMPORT_NACHNAME_MANDATORY<br/>- ASV_IMPORT_EMAIL_MANDATORY<br/>- ASV_IMPORT_GEBURTSTAG_MANDATORY<br/>- ASV_IMPORT_GESCHLECHT_MANDATORY<br/>- ASV_IMPORT_EINTRITTSDATUM_MANDATORY<br/>- ASV_IMPORT_SCHULABGANGAM_MANDATORY  |

Im Folgenden wird eine Detailbeschreibung der möglichen Schlüssel aufgelistet.

### WERT - DDD

DDD


## Datenbereinigungsmechanismus (CLEANUP_CONFIG)

Konfiguration des automatischen Datenbereinigungsmechanismus.

### Übersicht - CLEANUP_CONFIG

| CLEANUP_CONFIG |                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Konfigurationsort | GUI: Entitäten -> Konfiguration                                                                                                                                                                                                                                                                                                                                  |
| Konfig-Typ        | CLEANUP_CONFIG                                                                                                                                                                                                                                                                                                                                                   |
| Mögliche Schlüssel | - CLEANUP_SCHEDULE_ISACTIVE<br/>- CLEANUP_SCHEDULE_CRON<br/>- CLEANUP_SCHUELER_AFTER_X_DAYS_MARKED_AS_DELETED<br/>- CLEANUP_LOGEINTRAG_MAX_TO_KEEP<br/>- CLEANUP_LOGEINTRAG_AFTER_X_DAYS<br/>- CLEANUP_ASVIMPORT_MAX_TO_KEEP<br/>- CLEANUP_ASVIMPORT_AFTER_X_DAYS_UPLOADED<br/>- CLEANUP_EXPORTLAUF_MAX_TO_KEEP<br/>- CLEANUP_EXPORTLAUF_AFTER_X_DAYS_VALIDATED  |

Im Folgenden wird eine Detailbeschreibung der möglichen Schlüssel aufgelistet.

### WERT - DDD

DDD


## Basiskonfiguration (CORE_CONFIG)

Konfiguration des Regelsets zur Erstellung von eineindeutigen Benutzernamen, auf Basis der jeweiligen Vor- und Nachnamen der Schüler.


### Übersicht - CORE_CONFIG

| CORE_CONFIG |                                                                                                                                                                                                                                                                                                                                                                 |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Konfigurationsort | GUI: Entitäten -> Konfiguration                                                                                                                                                                                                                                                                                                                                 |
| Konfig-Typ        | CORE_CONFIG                                                                                                                                                                                                                                                                                                                                                  |
| Mögliche Schlüssel | - CORE_BENUTZERNAME_VORNAME_MIN_LEN<br/>- CORE_BENUTZERNAME_VORNAME_MAX_LEN<br/>- CORE_BENUTZERNAME_VORNAME_CUTOFF_CHARS<br/>- CORE_BENUTZERNAME_NACHNAME_MIN_LEN<br/>- CORE_BENUTZERNAME_NACHNAME_MAX_LEN<br/>- CORE_BENUTZERNAME_NACHNAME_CUTOFF_CHARS<br/>- CORE_BENUTZERNAME_MAX_LEN<br/>- CORE_BENUTZERNAME_SEPARATOR|

Im Folgenden wird eine Detailbeschreibung der möglichen Schlüssel aufgelistet.

### WERT - DDD

DDD


## Import-Export-Scheduler (IMPORTEXPORTTASK_CONFIG)

Konfiguration des Scheduled-Task für automatischen Import (aus ASV-SB) und Export (aller aktiven Exporter).

### Übersicht - IMPORTEXPORTTASK_CONFIG

| IMPORTEXPORTTASK_CONFIG |                                                                           |
|--------------------|---------------------------------------------------------------------------|
| Konfigurationsort  | GUI: Entitäten -> Konfiguration                                           |
| Konfig-Typ         | IMPORTEXPORTTASK_CONFIG                                                   |
| Mögliche Schlüssel | - IMPORTEXPORTTASK_SCHEDULE_ISACTIVE<br/>- IMPORTEXPORTTASK_SCHEDULE_CRON |

Im Folgenden wird eine Detailbeschreibung der möglichen Schlüssel aufgelistet.


TODO - ???

### WERT - IMPORTEXPORTTASK_SCHEDULE_ISACTIVE

| <!-- -->               | <!-- -->                                                             |
|------------------------|--------------------------------------------------------------|
| Konfig-Typ / Schlüssel | IMPORTEXPORTTASK_CONFIG / IMPORTEXPORTTASK_SCHEDULE_ISACTIVE |
| Standardwert           | false                                                        |
| Datentyp               | Boolean                                                      |
| Wertebereich:          | true / false                                                 |
| - true                 | Scheduled-Task für automatischen Import (aus ASV-SB) und Export (aller aktiven Exporter) ist aktiv                                                         |
| - false                | Scheduled-Task für automatischen Import (aus ASV-SB) und Export (aller aktiven Exporter) ist inaktiv                                                         |

### WERT - IMPORTEXPORTTASK_SCHEDULE_CRON

| <!-- -->               | <!-- -->                                                       |
|------------------------|----------------------------------------------------------------|
| Konfig-Typ / Schlüssel | IMPORTEXPORTTASK_CONFIG / IMPORTEXPORTTASK_SCHEDULE_CRON|
| Standardwert           | 0 2 * * * *                                                    |
| Datentyp               | CRON String                                                    |
| Wertebereich:          | Cron-Expression zur Bestimmung des Ausführungsplans. Siehe: DDD |

