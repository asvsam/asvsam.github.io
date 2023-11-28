---
layout: default
title: " - CleanupConfig"
parent: Benutzer-Handbuch
permalink: /asvsam/config_ui_konfiguration/CleanupConfig
nav_order: 120
---

# UI - Konfiguration - CleanupConfig

## ÜBERSICHT - Datenbereinigungsmechanismus (CLEANUP_CONFIG)

Konfiguration des automatischen Datenbereinigungsmechanismus.

| <!-- -->               | <!-- -->                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Konfigurationsort**  | GUI: Entitäten -> Konfiguration                                                                                                                                                                                                                                                                                                                                  |
| **Konfig-Typ**         | CLEANUP_CONFIG                                                                                                                                                                                                                                                                                                                                                   |
| **Mögliche Schlüssel** | - CLEANUP_SCHEDULE_ISACTIVE<br/>- CLEANUP_SCHEDULE_CRON<br/>- CLEANUP_SCHUELER_AFTER_X_DAYS_MARKED_AS_DELETED<br/>- CLEANUP_LOGEINTRAG_MAX_TO_KEEP<br/>- CLEANUP_LOGEINTRAG_AFTER_X_DAYS<br/>- CLEANUP_ASVIMPORT_MAX_TO_KEEP<br/>- CLEANUP_ASVIMPORT_AFTER_X_DAYS_UPLOADED<br/>- CLEANUP_EXPORTLAUF_MAX_TO_KEEP<br/>- CLEANUP_EXPORTLAUF_AFTER_X_DAYS_VALIDATDED |

Im Folgenden wird eine Detailbeschreibung der möglichen Schlüssel aufgelistet.

## WERT - CLEANUP_SCHEDULE_ISACTIVE

| <!-- -->                   | <!-- -->                                                                   |
|----------------------------|----------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | CLEANUP_CONFIG / CLEANUP_SCHEDULE_ISACTIVE                                 |
| **Standardwert**           | true                                                                       |
| **Datentyp**               | Boolean                                                                    |
| **Wertebereich:**          | true / false                                                               |
| - true                     | Scheduled-Task für automatische Datenbereinigung (in ASV-SAM) ist aktiv.   |
| - false                    | Scheduled-Task für automatische Datenbereinigung (in ASV-SAM) ist inaktiv. |

## WERT - CLEANUP_SCHEDULE_CRON

| <!-- -->                   | <!-- -->                                                                                                                                            |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | CLEANUP_CONFIG / CLEANUP_SCHEDULE_CRON                                                                                                              |
| **Standardwert**           | 0 0 * * * *                                                                                                                                         |
| **Datentyp**               | CRON String                                                                                                                                         |
| **Wertebereich:**          | Cron-Expression zur Bestimmung des Ausführungsplans.                                                                                                |
| - CronExpression           | Siehe [CronExpression](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/scheduling/support/CronExpression.html) |

## WERT - CLEANUP_SCHUELER_AFTER_X_DAYS_MARKED_AS_DELETED

| <!-- -->                   | <!-- -->                                                                                                                        |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | CLEANUP_CONFIG / CLEANUP_SCHUELER_AFTER_X_DAYS_MARKED_AS_DELETED                                                                |
| **Standardwert**           | 60                                                                                                                              |
| **Datentyp**               | Integer (>0)                                                                                                                    |
| **Wertebereich**           | Ganzzahl - Anzahl von Tagen nach einer Markierung eines Schülers als gelöscht, nach denen der Schüler in ASV-SAM gelöscht wird. |

## WERT - CLEANUP_LOGEINTRAG_MAX_TO_KEEP

| <!-- -->                   | <!-- -->                                                                                          |
|----------------------------|---------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | CLEANUP_CONFIG / CLEANUP_LOGEINTRAG_MAX_TO_KEEP                                                   |
| **Standardwert**           | 1000                                                                                              |
| **Datentyp**               | Integer (>0)                                                                                      |
| **Wertebereich**           | Ganzzahl - Maximale Anzahl von Log-Einträgen, welche nach dem Bereinigungslauf verbleiben sollen. |

## WERT - CLEANUP_LOGEINTRAG_AFTER_X_DAYS

| <!-- -->                   | <!-- -->                                                                            |
|----------------------------|-------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | CLEANUP_CONFIG / CLEANUP_LOGEINTRAG_AFTER_X_DAYS                                    |
| **Standardwert**           | 30                                                                                  |
| **Datentyp**               | Integer (>0)                                                                        |
| **Wertebereich**           | Ganzzahl - Maximales Alter in Tagen von Log-Einträgen die aufbewahrt werden sollen. |

## WERT - CLEANUP_ASVIMPORT_MAX_TO_KEEP

| <!-- -->                   | <!-- -->                                                                                        |
|----------------------------|-------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | CLEANUP_CONFIG / CLEANUP_ASVIMPORT_MAX_TO_KEEP                                                  |
| **Standardwert**           | 10                                                                                              |
| **Datentyp**               | Integer (>0)                                                                                    |
| **Wertebereich**           | Ganzzahl - Maximale Anzahl der ASV-Importe, welche nach dem Bereinigungslauf verbleiben sollen. |

## WERT - CLEANUP_ASVIMPORT_AFTER_X_DAYS_UPLOADED

| <!-- -->                   | <!-- -->                                                                                    |
|----------------------------|---------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | CLEANUP_CONFIG / CLEANUP_ASVIMPORT_AFTER_X_DAYS_UPLOADED                                    |
| **Standardwert**           | 90                                                                                          |
| **Datentyp**               | Integer (>0)                                                                                |
| **Wertebereich**           | Ganzzahl - Anzahl der Tage nach dem Upload-Datum, die ASV-Importe aufbewahrt werden sollen. |

## WERT - CLEANUP_EXPORTLAUF_MAX_TO_KEEP

| <!-- -->                   | <!-- -->                                                                                       |
|----------------------------|------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | CLEANUP_CONFIG / CLEANUP_EXPORTLAUF_MAX_TO_KEEP                                                |
| **Standardwert**           | 10                                                                                             |
| **Datentyp**               | Integer (>0)                                                                                   |
| **Wertebereich**           | Ganzzahl - Anzahl der Exportläufe, welche maximal nach dem Bereinigungslauf verbleiben sollen. |

## WERT - CLEANUP_EXPORTLAUF_AFTER_X_DAYS_VALIDATDED

| <!-- -->                   | <!-- -->                                                                                                |
|----------------------------|---------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | CLEANUP_CONFIG / CLEANUP_EXPORTLAUF_AFTER_X_DAYS_VALIDATDED                                             |
| **Standardwert**           | 90                                                                                                      |
| **Datentyp**               | Integer (>0)                                                                                            |
| **Wertebereich**           | Ganzzahl - Anzahl der Tage nach dem Validierungsdatum, welche die Exportläufe aufbewahrt werden sollen. |

