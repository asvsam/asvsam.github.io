---
layout: default
title: ASV-SAM Installer
parent: Installer/Setup-Handbuch
nav_order: 720
---

# Handbuch ASV-SAM - Installer

![Logo.png](../assets/images/Logo.png)


Der ASV-SAM-Installer dient der initialen Installation von ASV-SAM auf dem Zielsystem.


DDD



### Installation

**ETC Verzeichnisstruktur:**
```
/etc/asvsam/
/etc/asvsam/trusted.gpg
/etc/asvsam/asvsam-installer.conf
```

**ASV-SAM Daten Verzeichnisstruktur:**
```
/opt/asvsam
/opt/asvsam/asvsam-postgresql
/opt/asvsam/asvsam-postgresql/watchtower
/opt/asvsam/asvsam-postgresql/watchtower/watchtower.lifecycle.post-update.sh
/opt/asvsam/asvsam-postgresql/watchtower/watchtower.lifecycle.post-check.sh
/opt/asvsam/asvsam-postgresql/watchtower/watchtower.lifecycle.pre-check.sh
/opt/asvsam/asvsam-postgresql/watchtower/watchtower.lifecycle.pre-update.sh
/opt/asvsam/asvsam-postgresql/localbackup
/opt/asvsam/setup.sh
/opt/asvsam/asvsam-app
/opt/asvsam/asvsam-app/watchtower
/opt/asvsam/asvsam-app/watchtower/watchtower.lifecycle.post-update.sh
/opt/asvsam/asvsam-app/watchtower/watchtower.lifecycle.post-check.sh
/opt/asvsam/asvsam-app/watchtower/watchtower.lifecycle.pre-check.sh
/opt/asvsam/asvsam-app/watchtower/watchtower.lifecycle.pre-update.sh
/opt/asvsam/asvsam-app/localbackup
/opt/asvsam/scripts
/opt/asvsam/scripts/install_group_asvsam.sh
/opt/asvsam/scripts/functions_asvsam_setup.sh
/opt/asvsam/scripts/install_opt_asvsam.sh
/opt/asvsam/scripts/functions_misc.sh
/opt/asvsam/scripts/install_tools.sh
/opt/asvsam/scripts/install_docker.sh
/opt/asvsam/scripts/validate_prerequisites.sh
/opt/asvsam/scripts/functions_asvsam_installer.sh
/opt/asvsam/scripts/install_etc_asvsam.sh
/opt/asvsam/scripts/functions_variables.sh
/opt/asvsam/scripts/functions_cli.sh
/opt/asvsam/scripts/functions_dialog.sh
/opt/asvsam/scripts/functions_docker_yaml.sh
/opt/asvsam/scripts/config
/opt/asvsam/scripts/config/variables_asvsam_installer.csv
/opt/asvsam/scripts/config/app-prod-template.yml
/opt/asvsam/scripts/config/asvsam_setup_menu_config.csv
/opt/asvsam/scripts/config/asvsam_setup_dynamic_settings.env
/opt/asvsam/scripts/config/asvsam_setup_settings.env
/opt/asvsam/scripts/config/asvsam_setup_menu_config_email.csv
/opt/asvsam/scripts/config/asvsam_setup_menu_main.csv
/opt/asvsam/scripts/config/asvsam_setup_menu_config_general.csv
/opt/asvsam/scripts/config/asvsam_setup_menu_config_update.csv
/opt/asvsam/scripts/config/asvsam_setup_menu_config_asvbw.csv
/opt/asvsam/scripts/config/asvsam_installer_settings.env
/opt/asvsam/scripts/config/asvsam_setup_menu_config_backup.csv
/opt/asvsam/scripts/config/asvsam_setup_default_settings.env
```


### Backup

#### Backup/Restore des Programms und der Installation

### Docker-Compose YAML-Datei

Um neue Benutzer anlegen zu können müssen die folgenden Einstellungen in der Docker-Compose-Konfiguration 
korrekt gesetzt werden:

- SPRING_EMAIL_HOST=smtp.gmail.com
- SPRING_EMAIL_PORT=587
- SPRING_EMAIL_USERNAME=
- SPRING_EMAIL_PASSWORD=
- JHIPSTER_MAIL_FROM=
- JHIPSTER_MAIL_BASE-URL=

Postgres-Datenbank Verzeichnis

Docker-Image

Skripte, ...

#### Backup/Restore der Datenbank

Backup unter Verwendung von pg\_dump:
```
pg_dump \
    --host=<Datenbank-IP> \
    --port=<Datenbank-Port> \
    --username=<Datenbank-Benutzername> \
    --password <Datenbank-Name> \
    > <Backupdatenname>.sql
```

Restore unter Verwendung von psql:
```
psql \
    --host=<Datenbank-IP> \
    --port=<Datenbank-Port> \
    --username=<Datenbank-Benutzername> \
    --password <Datenbank-Name> \
    < <Backupdatenname>.sql
```

#### Backup/Restore der Daten über die Applikationslogik

##### Backup

GUI:

Administration -> API -> Suche (Filter by tag) „Backup” -> GET /api/backup getBackup

Kommandozeile:
```
# CONFIG
USER=<admin>
PASS=<password>
BASEURL=http://<IP-Adresse>:8080

# Authenticate
AUTH_TOKEN_RET=$(curl \
    -X 'POST' \
    -s ${BASEURL}/api/authenticate \
    -H 'accept: */*' \
    -H 'Content-Type: application/json' \
    -d "{\"username\":\"${USER}\",\"password\":\"${PASS}\",\"rememberMe\":false}")

AUTH_TOKEN=$(echo $AUTH_TOKEN_RET | sed -e "s/{\"id_token\":\"\(.*\)\"}/\1/g")
echo ${AUTH_TOKEN_RET}
echo ${AUTH_TOKEN}

# Backup
curl \
    -X 'GET' "${BASEURL}/api/backup" \
    -H "accept: */*" \
    -H "content-type: multipart/form-data" \
    -H "Authorization: Bearer ${AUTH_TOKEN}" \
    --output /home/user/asv-sam_backup.zip
```

##### Restore

GUI: Administration -> API -> Suche (Filter by tag) „Backup” -> POST /api/restore uploadData

Kommandozeile
```
# CONFIG
USER=<admin>
PASS=<password>
BASEURL=http://<IP-Adresse>:8080

# Authenticate
AUTH_TOKEN_RET=$(curl \
    -X 'POST' \
    -s ${BASEURL}/api/authenticate \
    -H 'accept: */*' \
    -H 'Content-Type: application/json' \
    -d "{\"username\":\"${USER}\",\"password\":\"${PASS}\",\"rememberMe\":false}")

AUTH_TOKEN=$(echo $AUTH_TOKEN_RET | sed -e "s/{\"id_token\":\"\(.*\)\"}/\1/g")
echo ${AUTH_TOKEN_RET}
echo ${AUTH_TOKEN}

# Restore
curl \
    -X 'POST' "${BASEURL}/api/restore" \
    -H "accept: */*" \
    -H "content-type: multipart/form-data" \
    -H "Authorization: Bearer ${AUTH_TOKEN}" \
    -F file=@/home/user/asv-sam_backup.zip
```
