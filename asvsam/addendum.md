---
layout: default
title: Angang
parent: Benutzer-Handbuch
permalink: /asvsam/addendum
nav_order: 300
---

# Anhang

## Links und Referenzen


| Referenz              | Referenz-Link                                                                                                                                                            |
|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reguläre Ausdrücke    | [*https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html*](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html)                       |
| Datumsformat          | [*https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html*](https://docs.oracle.com/javase/8/docs/api/java/time/format/DateTimeFormatter.html) |
| Docker                | ddd                                                                                                                                                                      |
| Docker-Compose        | ddd                                                                                                                                                                      |
| WebUntis Webseite     | [*https://www.untis.at/*](https://www.untis.at/)                                                                                                                         |
| Unterstützte Charsets | [*https://docs.oracle.com/javase/8/docs/technotes/guides/intl/encoding.doc.html*](https://docs.oracle.com/javase/8/docs/technotes/guides/intl/encoding.doc.html)         |


## CharSets

Relevante Charsets:
- ISO-8859-1=ISO-8859-1
- US-ASCII=US-ASCII
- UTF-8=UTF-8
- windows-1253=windows-1253

## Cron Ausdrücke
```
 ┌───────────── second (0-59)
 │ ┌───────────── minute (0 - 59)
 │ │ ┌───────────── hour (0 - 23)
 │ │ │ ┌───────────── day of the month (1 - 31)
 │ │ │ │ ┌───────────── month (1 - 12) (or JAN-DEC)
 │ │ │ │ │ ┌───────────── day of the week (0 - 7)
 │ │ │ │ │ │ (or MON-SUN -- 0 or 7 is Sunday)
 │ │ │ │ │ │
 * * * * * *

Beispiele:
 0 0 * * * *            # the top of every hour of every day.
 */10 * * * * *         # every ten seconds.
 0 0 8-10 * * *         # 8, 9 and 10 o'clock of every day.
 0 0 6,19 * * *         # 6:00 AM and 7:00 PM every day.
 0 0/30 8-10 * * *      # 8:00, 8:30, 9:00, 9:30, 10:00 and 10:30 every day.
 0 0 9-17 * * MON-FRI   # on the hour nine-to-five weekdays
 0 0 0 25 12 ?          # every Christmas Day at midnight
 0 0 0 L * *            # last day of the month at midnight
 0 0 0 L-3 * *          # third-to-last day of the month at midnight
 0 0 0 1W * *           # first weekday of the month at midnight
 0 0 0 LW * *           # last weekday of the month at midnight
 0 0 0 * * 5L           # last Friday of the month at midnight
 0 0 0 * * THUL         # last Thursday of the month at midnight
 0 0 0 ? * 5#2          # the second Friday in the month at midnight
 0 0 0 ? * MON#1        # the first Monday in the month at midnight
```
