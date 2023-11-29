---
layout: default
title: DEV - Dokumentation
parent: Entwickler-Handbuch
permalink: /dev_manual/dev_env_docu
nav_order: 2
---

# Dokumentation - asvsam.github.io

[![Deploy Jekyll site to Pages](https://github.com/asvsam/asvsam.github.io/actions/workflows/pages.yml/badge.svg)](https://github.com/asvsam/asvsam.github.io/actions/workflows/pages.yml)

## Lokale Entwicklungsumgebung und Test

**Voraussetzungen**
- ruby
- jekyll
- bundle

### Installation ruby

Für Details siehe: https://www.ruby-lang.org/de/documentation/installation/

```shell 
apt-get install rubygems
```
or
```shell 
yum -y install rubygems-devel
```

### Installation ruby pakete

```shell 
gem install bundler jekyll
```

### Git clone (Website repository)

```shell 
git clone https://github.com/asvsam/asvsam.github.io.git
```
or
```shell 
git clone git@github.com:asvsam/asvsam.github.io.git
```

### Local test Dokumentation

```shell
cd asvsam.github.io
bundle install
bundle exec jekyll serve
```

Öffnen folgender URL im Browser: [http://localhost:4000](http://localhost:4000)
