---
banner: "![[HomePage/wall.jpg]]"
banner_icon_: 🏠
---
# Welcome , Blake !

> `=date(today)`


## Tasks

> [!multi-column]
> 
> > [!error]+ Urgent
> > ```tasks
> > filename does not include 00 Plans
> > filename does not include 日记模板
> > path does not include Project
> > not done
> > due today
> 
> > [!attention]+ Approching
> > ```tasks
> > filename does not include 00 Plans
> > filename does not include 日记模板
> > path does not include Project
> > not done
> > due this week
> > due after today

> [!multi-column]
>
> > [!important]+ 
> > ```tasks
> > not done
> > filename does not include 00 Plans
> > path does not include Project
> > filename does not include 日记模板
> > status.name includes important
> 
> > [!seealso]+ 
> > ```tasks
> > not done
> > filename does not include 00 Plans
> > filename does not include 日记模板
> > path does not include Project
> > status.name does not include important

---

## Gallery

> [!multi-column]
> 
> > [!summary] Computer
> > - [Basic](Gallery/Computer/Basic/Basic.md)
> > - [Module](Gallery/Computer/Module/Module.md)
> > - [Tools](Gallery/Computer/Tool/Tools.md)
> 
> > [!summary] Physics
> > - 
> 
> > [!summary] Math
> > - 

> [!info] Recent File
> ```dataview
> list
> where file.mday >= date(today) - dur(1 week)
> sort file.mday desc
> limit 5
> ```

---

## Plans

> [!important] My Plans to be done
> ```tasks
filename includes 00 Plans
hide backlink
hide edit button

---

## Contributions

> [!success]  Contributions
> ```contributionGraph
title: 
graphType: default
dateRangeValue: 180
dateRangeType: LATEST_DAYS
startOfWeek: 1
showCellRuleIndicators: true
titleStyle:
  textAlign: left
  fontSize: 15px
  fontWeight: normal
dataSource:
  type: PAGE
  value: ""
  dateField: {}
fillTheScreen: true
enableMainContainerShadow: false
mainContainerStyle:
  backgroundColor: "#ffffff00"
cellStyleRules: []

```contributionGraph
title: Month
graphType: month-track
dateRangeValue: 180
dateRangeType: LATEST_DAYS
startOfWeek: 1
showCellRuleIndicators: true
titleStyle:
  textAlign: left
  fontSize: 15px
  fontWeight: normal
dataSource:
  type: PAGE
  value: ""
  dateField: {}
fillTheScreen: true
enableMainContainerShadow: true
cellStyleRules: []

```
