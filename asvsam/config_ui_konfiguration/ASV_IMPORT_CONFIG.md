---
layout: default
title: " - AsvImportConfig"
parent: Benutzer-Handbuch
permalink: /asvsam/config_ui_konfiguration/AsvImportConfig
nav_order: 110
---

# UI - Konfiguration - AsvImportConfig


## ÜBERSICHT - ASV-Importer-Konfiguration (ASV_IMPORT_CONFIG)

Konfiguration des ASV-Importers für die Übernahme der Daten aus ASV (Via CSV, XML oder ASB-Datenbank).

| <!-- -->               | <!-- -->                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Konfigurationsort**  | GUI: Entitäten -\> Konfiguration                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Konfig-Typ**         | ASV_IMPORT_CONFIG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Mögliche Schlüssel** | - ASV_IMPORT_GEBURTSTAG_DATEFORMAT<br/>- ASV_IMPORT_EINTRITTSDATUM_DATEFORMAT<br/>- ASV_IMPORT_AUSTRITTSDATUM_DATEFORMAT<br/>- ASV_IMPORT_EMAIL_REGEX<br/>- ASV_IMPORT_GESCHLECHT_REGEX<br/>- ASV_IMPORT_KLASSENBEZEICHNUNG_REGEX<br/>- ASV_IMPORT_SCHUELERID_REGEX<br/>- ASV_IMPORT_SCHUELERNR_REGEX<br/>- ASV_IMPORT_VORNAME_REGEX<br/>- ASV_IMPORT_NACHNAME_REGEX<br/>- ASV_IMPORT_KLASSENBEZEICHNUNG_MANDATORY<br/>- ASV_IMPORT_SCHUELERID_MANDATORY<br/>- ASV_IMPORT_SCHUELERNR_MANDATORY<br/>- ASV_IMPORT_VORNAME_MANDATORY<br/>- ASV_IMPORT_NACHNAME_MANDATORY<br/>- ASV_IMPORT_EMAIL_MANDATORY<br/>- ASV_IMPORT_GEBURTSTAG_MANDATORY<br/>- ASV_IMPORT_GESCHLECHT_MANDATORY<br/>- ASV_IMPORT_EINTRITTSDATUM_MANDATORY<br/>- ASV_IMPORT_SCHULABGANGAM_MANDATORY |

Im Folgenden wird eine Detailbeschreibung der möglichen Schlüssel aufgelistet.

TODO ???
ASVDB_IMPORT_SCHULJAHR_FILTER

## WERT - ASV_IMPORT_GEBURTSTAG_DATEFORMAT

| <!-- -->                   | <!-- -->                                                                                                |
|----------------------------|---------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | ASV_IMPORT_CONFIG / ASV_IMPORT_GEBURTSTAG_DATEFORMAT                                                    |
| **Standardwert**           | dd.MM.yyyy                                                                                              |
| **Datentyp**               | Datumsformat String                                                                                     |
| **Wertebereich:**          | Format der Datenfeldes Geburtstag.                                                                      |
| - Datumsformat             | Siehe [Datumsformat](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html) |

## WERT - ASV_IMPORT_EINTRITTSDATUM_DATEFORMAT

| <!-- -->                   | <!-- -->                                                                                                |
|----------------------------|---------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | ASV_IMPORT_CONFIG / ASV_IMPORT_EINTRITTSDATUM_DATEFORMAT                                                |
| **Standardwert**           | dd.MM.yyyy                                                                                              |
| **Datentyp**               | Datumsformat String                                                                                     |
| **Wertebereich:**          | Format der Datenfeldes Eintrittsdatum.                                                                  |
| - Datumsformat             | Siehe [Datumsformat](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html) |

## WERT - ASV_IMPORT_AUSTRITTSDATUM_DATEFORMAT

| <!-- -->                   | <!-- -->                                                                                                |
|----------------------------|---------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | ASV_IMPORT_CONFIG / ASV_IMPORT_AUSTRITTSDATUM_DATEFORMAT                                                |
| **Standardwert**           | dd.MM.yyyy                                                                                              |
| **Datentyp**               | Datumsformat String                                                                                     |
| **Wertebereich:**          | Format der Datenfeldes Austrittsdatum.                                                                  |
| - Datumsformat             | Siehe [Datumsformat](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html) |

## WERT - ASV_IMPORT_EMAIL_REGEX

| <!-- -->                   | <!-- -->                                                                                           |
|----------------------------|----------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | ASV_IMPORT_CONFIG / ASV_IMPORT_EMAIL_REGEX                                                         |
| **Standardwert**           | ;^[A-Za-z0-9_.+-]+@[A-Za-z0-9-.]+\.[A-Za-z]+$                                                      |
| **Datentyp**               | Regulärer Ausdruck                                                                                 |
| **Wertebereich:**          | Regulärer Ausdruck zur Validierung des Datenfeldes Email.                                          |
| - Regulärer Ausdruck       | Siehe [Regulärer Ausdruck](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) |

## WERT - ASV_IMPORT_GESCHLECHT_REGEX

| <!-- -->                   | <!-- -->                                                                                           |
|----------------------------|----------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | ASV_IMPORT_CONFIG / ASV_IMPORT_GESCHLECHT_REGEX                                                    |
| **Standardwert**           | ^[MWO]$                                                                                            |
| **Datentyp**               | Regulärer Ausdruck                                                                                 |
| **Wertebereich:**          | Regulärer Ausdruck zur Validierung des Datenfeldes Geschlecht.                                     |
| - Regulärer Ausdruck       | Siehe [Regulärer Ausdruck](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) |

## WERT - ASV_IMPORT_KLASSENBEZEICHNUNG_REGEX

| <!-- -->                   | <!-- -->                                                                                           |
|----------------------------|----------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | ASV_IMPORT_CONFIG / ASV_IMPORT_KLASSENBEZEICHNUNG_REGEX                                            |
| **Standardwert**           | ^.\*$                                                                                              |
| **Datentyp**               | Regulärer Ausdruck                                                                                 |
| **Wertebereich:**          | Regulärer Ausdruck zur Validierung des Datenfeldes Klassenbezeichnung.                             |
| - Regulärer Ausdruck       | Siehe [Regulärer Ausdruck](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) |

## WERT - ASV_IMPORT_SCHUELERID_REGEX

| <!-- -->                   | <!-- -->                                                                                           |
|----------------------------|----------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | ASV_IMPORT_CONFIG / ASV_IMPORT_SCHUELERID_REGEX                                                    |
| **Standardwert**           | ^[a-f0-9]{8}-[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{8}-[a-f0-9]{4}$                                      |
| **Datentyp**               | Regulärer Ausdruck                                                                                 |
| **Wertebereich:**          | Regulärer Ausdruck zur Validierung des Datenfeldes SchülerId.                                      |
| - Regulärer Ausdruck       | Siehe [Regulärer Ausdruck](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) |

## WERT - ASV_IMPORT_SCHUELERNR_REGEX

| <!-- -->                   | <!-- -->                                                                                           |
|----------------------------|----------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | ASV_IMPORT_CONFIG / ASV_IMPORT_SCHUELERNR_REGEX                                                    |
| **Standardwert**           | ^.\*$                                                                                              |
| **Datentyp**               | Regulärer Ausdruck                                                                                 |
| **Wertebereich:**          | Regulärer Ausdruck zur Validierung des Datenfeldes SchülerINr.                                     |
| - Regulärer Ausdruck       | Siehe [Regulärer Ausdruck](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) |

## WERT - ASV_IMPORT_VORNAME_REGEX

| <!-- -->                   | <!-- -->                                                                                           |
|----------------------------|----------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | ASV_IMPORT_CONFIG / ASV_IMPORT_VORNAME_REGEX                                                       |
| **Standardwert**           | ^.\*$                                                                                              |
| **Datentyp**               | Regulärer Ausdruck                                                                                 |
| **Wertebereich:**          | Regulärer Ausdruck zur Validierung des Datenfeldes Vorname.                                        |
| - Regulärer Ausdruck       | Siehe [Regulärer Ausdruck](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) |

## WERT - ASV_IMPORT_NACHNAME_REGEX

| <!-- -->                   | <!-- -->                                                                                           |
|----------------------------|----------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | ASV_IMPORT_CONFIG / ASV_IMPORT_NACHNAME_REGEX                                                      |
| **Standardwert**           | ^.\*$                                                                                              |
| **Datentyp**               | Regulärer Ausdruck                                                                                 |
| **Wertebereich:**          | Regulärer Ausdruck zur Validierung des Datenfeldes Nachname.                                       |
| - Regulärer Ausdruck       | Siehe [Regulärer Ausdruck](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) |

## WERT - ASV_IMPORT_KLASSENBEZEICHNUNG_MANDATORY

| <!-- -->                   | <!-- -->                                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | IMPORTEXPORTTASK_CONFIG / ASV_IMPORT_KLASSENBEZEICHNUNG_MANDATORY                                                     |
| **Standardwert**           | true                                                                                                                  |
| **Datentyp**               | Boolean                                                                                                               |
| **Wertebereich:**          | true / false                                                                                                          |
| - true                     | Datenfeld Klassenbezeichnung ist obligatorisch. Nichtvorhandensein eines Wertes bedingt eine fehlerhafte Validierung. |
| - false                    | Datenfeld Klassenbezeichnung ist optional.                                                                            |

## WERT - ASV_IMPORT_SCHUELERID_MANDATORY

| <!-- -->                   | <!-- -->                                                                                                     |
|----------------------------|--------------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | IMPORTEXPORTTASK_CONFIG / ASV_IMPORT_SCHUELERID_MANDATORY                                                    |
| **Standardwert**           | true                                                                                                         |
| **Datentyp**               | Boolean                                                                                                      |
| **Wertebereich:**          | true / false                                                                                                 |
| - true                     | Datenfeld SchülerId ist obligatorisch. Nichtvorhandensein eines Wertes bedingt eine fehlerhafte Validierung. |
| - false                    | Datenfeld SchülerId ist optional.                                                                            |

## WERT - ASV_IMPORT_SCHUELERNR_MANDATORY

| <!-- -->                   | <!-- -->                                                                                                     |
|----------------------------|--------------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | IMPORTEXPORTTASK_CONFIG / ASV_IMPORT_SCHUELERNR_MANDATORY                                                    |
| **Standardwert**           | false                                                                                                        |
| **Datentyp**               | Boolean                                                                                                      |
| **Wertebereich:**          | true / false                                                                                                 |
| - true                     | Datenfeld SchülerNr ist obligatorisch. Nichtvorhandensein eines Wertes bedingt eine fehlerhafte Validierung. |
| - false                    | Datenfeld SchülerNr ist optional.                                                                            |

## WERT - ASV_IMPORT_VORNAME_MANDATORY

| <!-- -->                   | <!-- -->                                                                                                   |
|----------------------------|------------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | IMPORTEXPORTTASK_CONFIG / ASV_IMPORT_VORNAME_MANDATORY                                                     |
| **Standardwert**           | true                                                                                                       |
| **Datentyp**               | Boolean                                                                                                    |
| **Wertebereich:**          | true / false                                                                                               |
| - true                     | Datenfeld Vorname ist obligatorisch. Nichtvorhandensein eines Wertes bedingt eine fehlerhafte Validierung. |
| - false                    | Datenfeld Vorname ist optional.                                                                            |

## WERT -

| <!-- -->                   | <!-- -->                                                                                                    |
|----------------------------|-------------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | IMPORTEXPORTTASK_CONFIG / ASV_IMPORT_NACHNAME_MANDATORY                                                     |
| **Standardwert**           | true                                                                                                        |
| **Datentyp**               | Boolean                                                                                                     |
| **Wertebereich:**          | true / false                                                                                                |
| - true                     | Datenfeld Nachname ist obligatorisch. Nichtvorhandensein eines Wertes bedingt eine fehlerhafte Validierung. |
| - false                    | Datenfeld Nachname ist optional.                                                                            |

## WERT - ASV_IMPORT_EMAIL_MANDATORY

| <!-- -->                   | <!-- -->                                                                                                 |
|----------------------------|----------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | IMPORTEXPORTTASK_CONFIG / ASV_IMPORT_EMAIL_MANDATORY                                                     |
| **Standardwert**           | true                                                                                                     |
| **Datentyp**               | Boolean                                                                                                  |
| **Wertebereich:**          | true / false                                                                                             |
| - true                     | Datenfeld Email ist obligatorisch. Nichtvorhandensein eines Wertes bedingt eine fehlerhafte Validierung. |
| - false                    | Datenfeld Email ist optional.                                                                            |

## WERT - ASV_IMPORT_GEBURTSTAG_MANDATORY

| <!-- -->                   | <!-- -->                                                                                                      |
|----------------------------|---------------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | IMPORTEXPORTTASK_CONFIG / ASV_IMPORT_GEBURTSTAG_MANDATORY                                                     |
| **Standardwert**           | true                                                                                                          |
| **Datentyp**               | Boolean                                                                                                       |
| **Wertebereich:**          | true / false                                                                                                  |
| - true                     | Datenfeld Geburtstag ist obligatorisch. Nichtvorhandensein eines Wertes bedingt eine fehlerhafte Validierung. |
| - false                    | Datenfeld Geburtstag ist optional.                                                                            |

## WERT - ASV_IMPORT_GESCHLECHT_MANDATORY

| <!-- -->                   | <!-- -->                                                                                                      |
|----------------------------|---------------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | IMPORTEXPORTTASK_CONFIG / ASV_IMPORT_GESCHLECHT_MANDATORY                                                     |
| **Standardwert**           | true                                                                                                          |
| **Datentyp**               | Boolean                                                                                                       |
| **Wertebereich:**          | true / false                                                                                                  |
| - true                     | Datenfeld Geschlecht ist obligatorisch. Nichtvorhandensein eines Wertes bedingt eine fehlerhafte Validierung. |
| - false                    | Datenfeld Geschlecht ist optional.                                                                            |

## WERT - ASV_IMPORT_EINTRITTSDATUM_MANDATORY

| <!-- -->                   | <!-- -->                                                                                                          |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | IMPORTEXPORTTASK_CONFIG / ASV_IMPORT_EINTRITTSDATUM_MANDATORY                                                     |
| **Standardwert**           | true                                                                                                              |
| **Datentyp**               | Boolean                                                                                                           |
| **Wertebereich:**          | true / false                                                                                                      |
| - true                     | Datenfeld Eintrittsdatum ist obligatorisch. Nichtvorhandensein eines Wertes bedingt eine fehlerhafte Validierung. |
| - false                    | Datenfeld Eintrittsdatum ist optional.                                                                            |

## WERT - ASV_IMPORT_SCHULABGANGAM_MANDATORY

| <!-- -->                   | <!-- -->                                                                                                         |
|----------------------------|------------------------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | IMPORTEXPORTTASK_CONFIG / ASV_IMPORT_SCHULABGANGAM_MANDATORY                                                     |
| **Standardwert**           | true                                                                                                             |
| **Datentyp**               | Boolean                                                                                                          |
| **Wertebereich:**          | true / false                                                                                                     |
| - true                     | Datenfeld SchulabgangAm ist obligatorisch. Nichtvorhandensein eines Wertes bedingt eine fehlerhafte Validierung. |
| - false                    | Datenfeld SchulabgangAm ist optional.                                                                            |

## WERT - ASV_IMPORT_GESCHLECHT_MAPPING_MAENNLICH

| <!-- -->                   | <!-- -->                                                                                           |
|----------------------------|----------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | ASV_IMPORT_CONFIG / ASV_IMPORT_GESCHLECHT_MAPPING_MAENNLICH                                        |
| **Standardwert**           | ^[Mm]\|[Mm]ännlich\|[Mm]aennlich$                                                                  |
| **Datentyp**               | Regulärer Ausdruck                                                                                 |
| **Wertebereich:**          | Regulärer Ausdruck zur Erkennung des Wertes männlich Geschlecht für Datenfeldes Geschlecht.        |
| - Regulärer Ausdruck       | Siehe [Regulärer Ausdruck](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) |

## WERT - ASV_IMPORT_GESCHLECHT_MAPPING_WEIBLICH

| <!-- -->                   | <!-- -->                                                                                           |
|----------------------------|----------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | ASV_IMPORT_CONFIG / ASV_IMPORT_GESCHLECHT_MAPPING_WEIBLICH                                         |
| **Standardwert**           | ^[Ww]\|[Ww]eiblich$                                                                                |
| **Datentyp**               | Regulärer Ausdruck                                                                                 |
| **Wertebereich:**          | Regulärer Ausdruck zur Erkennung des Wertes weiblich Geschlecht für Datenfeldes Geschlecht.        |
| - Regulärer Ausdruck       | Siehe [Regulärer Ausdruck](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) |

## WERT - ASV_IMPORT_GESCHLECHT_MAPPING_DIVERS

| <!-- -->                   | <!-- -->                                                                                           |
|----------------------------|----------------------------------------------------------------------------------------------------|
| **Konfig-Typ / Schlüssel** | ASV_IMPORT_CONFIG / ASV_IMPORT_GESCHLECHT_MAPPING_DIVERS                                           |
| **Standardwert**           | ^[Dd]\|[Dd]ivers$                                                                                  |
| **Datentyp**               | Regulärer Ausdruck                                                                                 |
| **Wertebereich:**          | Regulärer Ausdruck zur Erkennung des Wertes divers Geschlecht für Datenfeldes Geschlecht.          |
| - Regulärer Ausdruck       | Siehe [Regulärer Ausdruck](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) |

