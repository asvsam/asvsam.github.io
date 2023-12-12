---
layout: default
title: TODO's Entwickler-Handbuch
parent: Entwickler-Handbuch
permalink: /dev_manual/todos
nav_order: 800
---

# Themen (TODO's)

- Release-Flow
  - Git-Commits
  - GitHub-Release
  - GPG-Signing
  - Automation
  - Testing
- Vorgaben
- Erklärung des Codes und der Funktionsweise
- Kontaktdaten und wie man als Entwickler dabei sein kann

- Github environment

- Entwicklungsumgebung - Entwicklersystem



# DataBo ERD

```mermaid
---
title: DataBo ERD
---
erDiagram

    DataBo {
        String valError
        string sourceName
        string targetName
    }

    DataBo ||--|{ DataLineBo : "has_by_Key_as_Map"
    DataLineBo {
        String idInternal
        String idConstructed
        String idExternal
        Map_String_DataLineAttrBo valueMap
        String ValError
    }

    DataLineBo ||--|{ DataLineAttrBo : "has_by_Key_as_Map"
    DataLineAttrBo {
        String name
        String value
        String valueOriginal
        String valError
    }
    
    DataBo ||--o{ DataActionEntry : "has"
    DataActionEntry {
        String name
        String configDetail
        String resultNote
        Instant timeStamp
    }

    DataBoCompareResult ||--o{ DataBo : "is source"
    DataBoCompareResult ||--o{ DataBo : "is target"
    DataBoCompareResult ||--o{ DataBo : "to be added"
    DataBoCompareResult ||--o{ DataBo : "to be deleted"
    DataBoCompareResult ||--o{ DataBo : "to be updated"
    DataBoCompareResult ||--o{ DataBo : "to do nothing"
    DataBoCompareResult ||--o{ DataBo : "already deleted"
    DataBoCompareResult ||--o{ DataLineBo : "delta"
    DataBoCompareResult {
        DataBo dataBoSource
        DataBo dataBoTarget
        DataBo dataBoToBeAdded
        DataBo dataBoToBeDelete
        DataBo dataBoToBeUpdated
        DataBo dataBoToDoNothing
        DataBo dataBoAlreadyDeleted
        Map_String_DataBoLineDelta dataBoDeltaMap
    }
```

# Funktionsweise

| Objekt              | Funktionales Equivalent                                 |
|---------------------|---------------------------------------------------------|
| DataBoCompareResult | Deltaset von Tabellen zur Beschreibung der Unterschiede |
| DataActionEntry     | Aktionslogbuch                                          |
| DataBo              | Tabelle                                                 |
| DataLineBo          | Zeile                                                   |
| DataLineAttrBo      | Zelle                                                   |

# DataBo class diagram

```mermaid
---
title: DataBo class diagram
---
classDiagram

    class DataBo {
        +String beakColor
        +swim()
        +quack()
    }

    DataBo "1" --> "1..*"DataLineBo : has_by_Key_as_Map
    class DataLineBo {
        -int sizeInFeet
        -canEat()
    }

    DataLineBo "1" --> "1..*" DataLineAttrBo : has_by_Key_as_Map
    class DataLineAttrBo {
        -int sizeInFeet
        -canEat()
    }
    
    DataBo "1" --> "*" DataActionEntry : has
    class DataActionEntry {
        +bool is_wild
        +run()
    }

    DataBoCompareResult "1" --> "*" DataBo : is source
    DataBoCompareResult "1" --> "*" DataBo : is target
    DataBoCompareResult "1" --> "*" DataBo : to be added
    DataBoCompareResult "1" --> "*" DataBo : to be deleted
    DataBoCompareResult "1" --> "*" DataBo : to be updated
    DataBoCompareResult "1" --> "*" DataBo : to do nothing
    DataBoCompareResult "1" --> "*" DataBo : already deleted
    DataBoCompareResult "1" --> "*" DataLineBo : delta
    class DataBoCompareResult {
        -DataBo dataBoSource
        -DataBo dataBoTarget

        -DataBo dataBoToBeAdded
        -DataBo dataBoToBeDelete
        -DataBo dataBoToBeUpdated
        -DataBo dataBoToDoNothing
        -DataBo dataBoAlreadyDeleted

        -Map<String, DataBoLineDelta> dataBoDeltaMap

        +DataBoCompareResult(DataBo dataBoSource, DataBo dataBoTarget)
    }
```


```mermaid
---
title: gitGraph
---
gitGraph
    commit id: "1"
    commit id: "2"
    branch nice_feature
    checkout nice_feature
    commit id: "3"
    checkout main
    commit id: "4"
    checkout nice_feature
    branch very_nice_feature
    checkout very_nice_feature
    commit id: "5"
    checkout main
    commit id: "6"
    checkout nice_feature
    commit id: "7"
    checkout main
    merge nice_feature id: "customID" tag: "customTag" type: REVERSE
    checkout very_nice_feature
    commit id: "8"
    checkout main
    commit id: "9"
```

```mermaid
---
title: gitGraph
---
gitGraph

commit id: "m.1" tag: "1.0.1" type: HIGHLIGHT
branch hotfix
branch release
branch develop
checkout develop
commit id: "d.1"
commit id: "d.2"
commit id: "d.3"
branch feature_1
branch feature_2
commit id: "f2.1"
checkout develop
commit id: "d.4"
checkout hotfix
commit id: "h.1"
checkout main
merge hotfix id: "m.2" tag: "1.0.2" type: NORMAL

    checkout feature_2
    commit id: "f2.2"
checkout feature_1
commit id: "f1.2"
#branch feature_2
    checkout develop
    merge hotfix id: "d.5" type: NORMAL
    checkout feature_1
    commit id: "f1.3"
    checkout develop
    merge feature_1 id: "d.6" type: NORMAL
checkout release
    merge main id: "r.1" type: NORMAL
    merge feature_1 id: "r.2" tag: "1.1.pre" type: NORMAL
commit id: "r.3"
checkout develop
    merge release id: "d.7" type: NORMAL

    checkout feature_2
    commit id: "f2.3"
checkout release
commit id: "r.4"
checkout feature_1
    merge develop id: "f1.4" type: NORMAL
    commit id: "f1.5"
    checkout release
    commit id: "r.5"
    checkout develop
    merge release id: "d1.8" type: NORMAL
    checkout main
    merge release id: "m.3" tag: "1.1.0" type: NORMAL
checkout feature_1
commit id: "f1.6"
checkout feature_2
commit id: "f2.4"
checkout develop
    merge feature_1 id: "d.9" type: NORMAL
    merge feature_2 id: "d.10" type: NORMAL
checkout release
    merge develop id: "1.6" type: NORMAL
checkout develop
    merge release id: "d.11" type: NORMAL
    checkout main
    merge release id: "m.4" tag: "1.1.1" type: NORMAL
```

