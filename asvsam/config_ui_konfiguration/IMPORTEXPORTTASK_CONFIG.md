---
layout: default
title: " - ImportExportTask"
parent: Benutzer-Handbuch
permalink: /asvsam/config_ui_konfiguration/ImportExportTask
nav_order: 140
---

# UI - Konfiguration - ImportExportTask


## ÜBERSICHT - Import-Export-Scheduler (IMPORTEXPORTTASK_CONFIG)

Konfiguration des Scheduled-Task für automatischen Import (aus ASV-BW) und Export (aller aktiven Exporter).

| <!-- -->               | <!-- -->                                                                  |
|------------------------|---------------------------------------------------------------------------|
| **Konfigurationsort**  | GUI: Entitäten -> Konfiguration                                           |
| **Konfig-Typ**         | IMPORTEXPORTTASK_CONFIG                                                   |
| **Mögliche Schlüssel** | - IMPORTEXPORTTASK_SCHEDULE_ISACTIVE<br/>- IMPORTEXPORTTASK_SCHEDULE_CRON |

Im Folgenden wird eine Detailbeschreibung der möglichen Schlüssel aufgelistet.

## WERT - IMPORTEXPORTTASK_SCHEDULE_ISACTIVE

| <!-- -->                   | <!-- -->                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | IMPORTEXPORTTASK_CONFIG / IMPORTEXPORTTASK_SCHEDULE_ISACTIVE                                         |
| **Standardwert**           | false                                                                                                |
| **Datentyp**               | Boolean                                                                                              |
| **Wertebereich:**          | true / false                                                                                         |
| - true                     | Scheduled-Task für automatischen Import (aus ASV-SB) und Export (aller aktiven Exporter) ist aktiv   |
| - false                    | Scheduled-Task für automatischen Import (aus ASV-SB) und Export (aller aktiven Exporter) ist inaktiv |

## WERT - IMPORTEXPORTTASK_SCHEDULE_CRON

| <!-- -->                   | <!-- -->                                                                                                                                            |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | IMPORTEXPORTTASK_CONFIG / IMPORTEXPORTTASK_SCHEDULE_CRON                                                                                            |
| **Standardwert**           | 0 2 * * * *                                                                                                                                         |
| **Datentyp**               | CRON String                                                                                                                                         |
| **Wertebereich:**          | Cron-Expression zur Bestimmung des Ausführungsplans.                                                                                                |
| - CronExpression           | Siehe [CronExpression](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/scheduling/support/CronExpression.html) |
