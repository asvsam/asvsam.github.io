---
layout: default
title: DEV - Entwicklersystem
parent: Entwickler-Handbuch
permalink: /dev_manual/dev_env_workstation
nav_order: 3
---

# Entwicklungsumgebung - Entwicklersystem

- Environment Install
  - Java (JDK 11)
  - Docker (v2)
  - NodeJs (v18)
  - Git-Client
  - GPG install
  - SSH-Client
  - Entwicklungsumgebung-IDE ihrer Wahl

- Optional
  - GitHub.cli


## Installation Java JDK
Siehe: https://www.java.com/de/download/help/download_options_de.html

oder via WinGet:
```shell 
winget install EclipseAdoptium.Temurin.11.JDK
winget install EclipseAdoptium.Temurin.19.JDK
```

## Installation Docker
Es gib verschiedene Optionen. Z.B.:
 * 1 DockerDesktop
 * 2 Unter Windows WSL2 plus Docker installation in Linux

### 1 - Installation DockerDesktop
Siehe: https://docs.docker.com/engine/install/

oder via WinGet:
```shell 
winget install Docker.DockerDesktop
```

### 2 - Installation WSL2 plus Docker installation in Linux
via WinGet:
```shell 
winget install Debian.Debian
```

## Installation NodeJs
Siehe: https://nodejs.org/en/download

oder via WinGet:
```shell 
winget install OpenJS.NodeJS.LTS
```

## Installation Git-Client
Siehe: https://git-scm.com/book/de/v2/Erste-Schritte-Git-installieren

oder via WinGet:
```shell 
winget install Git.Git
```



## Installation GPG
Siehe: https://gnupg.org/download/ und https://gpg4win.org/download.html

oder via WinGet:
```shell 
winget install GnuPG.GnuPG
winget install GnuPG.Gpg4win
```

## Installation SSH-Client
Siehe Z.B.: https://www.putty.org/

oder via WinGet:
```shell 
winget install PuTTY.PuTTY
```


## Installalion GitHub-CLI
Siehe: https://cli.github.com/

oder via WinGet:
```shell 
winget install GitHub.cli
```

