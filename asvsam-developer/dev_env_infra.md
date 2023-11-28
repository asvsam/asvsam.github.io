---
layout: default
title: DEV - Infrastruktur
parent: Entwickler-Handbuch
permalink: /dev_manual/dev_env_infra
nav_order: 3
---

# Entwicklungsumgebung - Infrastruktur

## E-Mail Server

**Voraussetzungen**

- Dockerumgebung
- Internetzugang

### Run DB-Docker-Container (via Docker-Compose)

docker-compose.yml:
```yaml
version: '3.0'
services:
  asvsam-smtp:
    image: maildev/maildev
    restart: unless-stopped
    ports:
      - 1025:1025
      - 1080:1080
```

### Run DB-Docker-Container (via Docker)

```shell
docker run --name asvsam-smtp -d -p 1025:1025 -p 1080:1080 maildev/maildev
```

### ASV-SAM Konfiguration

Einstellung des verwendeten Email Servers (Möglichkeiten je nach Setup):
- Email-Server = asvsam-smtp:1025
- Email-Server = localhost:1025
- Email-Server = \<hostname>:1025
- Email-Server = \<ip-adresse>:1025
- Email-Server = host.docker.internal:1025


## ASV-Datenbank

Für die Entwicklung auf in einem nicht produktiven Umfeld ist es empfehlenswert eine ASV-Datenbankkopie zu erstellen und lokal in Form eines Docker-Containers laufen zu lassen. Die Installation und das Setup werden im Folgenden genauer beschrieben.

**Voraussetzungen**

- Dockerumgebung
- Internetzugang
- Dockerumgebung
- Internetzugang
- Postgres-SQL Client-Tools (psql, pg_dump)
- ASV-Datenbank SQL-Export oder Zugang zur ASV-Datenbank, inkl. der
- Zugangsdaten für die ASV-DB-Datenbank Quelle:
    - Datenbankhostname o. -IP
    - Datenbankport
    - Datenbankname
    - Datenbankbenutzer
    - Datenbankpasswort
- Zugangsdaten für die ASV-DB-Datenbank Ziel:
    - Datenbankname
    - Datenbankbenutzer
    - Datenbankpasswort
    - Datenbankport

### Erstellen eines ASV-Datenbank-Exports

```shell
pg_dump --host=asvdatenbankhost --port=5433 --username=asvdbuser --password asvdbname > asv_backup.sql
```

### Run DB-Docker-Container

```shell
docker run --name asv-source-postgres -e POSTGRES_USER=asvdbuser -e POSTGRES_PASSWORD=asvdbpassword -e POSTGRES_DB=asvdbname -d -p 15432:5432 postgres:11.14
```

### Import ASV Daten in Datenbank-Docker-Container

```shell
psql -h localhost -p 15432 -U asvdbuser asvdbname < asv_backup.sql
```

## PaedMl Service-Mock

```shell
cd asvsam\src\main\docker\paedml-mock
docker-compose up -d
```


## WebUntis-API

Für die Entwicklung auf in einem nicht produktiven Umfeld ist es empfehlenswert einen Entwickler-Zugang von WebUntis zu
beantragen. Kontaktinformationen können der WebUntis-Webseite ([https://www.untis.at/](https://www.untis.at/)) entnommen werden.

