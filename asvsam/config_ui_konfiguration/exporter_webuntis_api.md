---
layout: default
title: " - Exporter - WebUntis (API)"
parent: Benutzer-Handbuch
permalink: /asvsam/config_ui_konfiguration/ExporterWebUntisApi
nav_order: 210
---

TODO
{: .label .label-red }


Todo:
- Bilder
- Ausformulieren


# UI - Konfiguration - Exporte WebUntis (API)

## WebUntis UI - Einrichtung der Plattform Applikation

Prozess:
- Open WebUntis Web-Oberfläche
- Administration -> Plattform
- Neue Plattform (* - Plus-Symbol)
- Auswahl von ASV-SAM (Schulaccount.Manager)
- Aktivieren der Applikation (Schalter)
- Kopieren der Zugangsdaten
- Speichern (Button)
- Auf der Seite Haftungsausschluss
  - Ich habe verstanden anhaken
  - Passwort kopieren
  - Passwort gesichert anhaken
  - Mit OK (Button) bestätigen

-> Fertig in WebUntis UI

Folgende Infommationen sollten sie nun verfügbar haben:
- WEBUNTIS_TENANT_ID
- WEBUNTIS_SERVER_URL
- WEBUNTIS_OIDC_SECRET
- WEBUNTIS_API_PASSWORT

## ASV-SAM UI - Einrichtung des WebUntis Exporters

- WEBUNTIS_TENANT_ID
- WEBUNTIS_SERVER_URL
- WEBUNTIS_OIDC_SECRET
- WEBUNTIS_API_PASSWORT
- WEBUNTIS_ADMIN_EMAIL_VERANTWORLICHER
- ??? Was ist der fachliche Schlüssel zur eindeutigen identifikation von Schülern, der verwendet werden soll. Z.B.:
  - WEBUNTIS.SHORTNAME
  - WEBUNTIS.EXTERNKEY

```json
{
    "accessTokenRefreshGraceSeconds": 60,
    "apiPassword": "<###_WEBUNTIS_API_PASSWORT_###>",
    "apiUri": "https://api.webuntis.com/WebUntis/api",
    "apiUser": "ASVConnector",
    "authorizationGrantType": "client_credentials",
    "clientId": "ASVConnector",
    "clientSecret": "<###_WEBUNTIS_OIDC_SECRET_###>",
    "compareDefinitionList": [
        "WEBUNTIS.EXTERNKEY",
        "WEBUNTIS.ADULT",
        "WEBUNTIS.ACTIVE",
        "WEBUNTIS.FORENAME",
        "WEBUNTIS.LASTNAME",
        "WEBUNTIS.SHORTNAME",
        "WEBUNTIS.GENDER",
        "WEBUNTIS.BIRTHDATE",
        "WEBUNTIS.ENTRYDATE",
        "WEBUNTIS.EXITDATE",
        "WEBUNTIS.CLASS",
        "WEBUNTIS.EMAIL"
    ],
    "keyDefinitionList": [
        "WEBUNTIS.EXTERNKEY"
    ],
    "recipients": [
        "<###_WEBUNTIS_ADMIN_EMAIL_VERANTWORLICHER_###>"
    ],
    "resource": "https://api.webuntis.com/WebUntis/api",
    "scope": "roster-core",
    "tokenUri": "<###_WEBUNTIS_SERVER_URL_###>/api/sso/v2/###_WEBUNTIS_TENANT_ID_###>/token",
    "verifySslHostTrust": true
}
```

Test-Modus

Aktivieren


 