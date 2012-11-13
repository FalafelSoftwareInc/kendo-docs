---
title: stockChart-navigator-seriesItem-tooltip
slug: jsp-stockChart-navigator-seriesItem-tooltip
tags: api, java
publish: true
---

# \<kendo:stockChart-navigator-seriesItem-tooltip\>
A JSP tag representing Kendo Tooltip.

#### Example
    <kendo:stockChart-navigator-seriesItem>
        <kendo:stockChart-navigator-seriesItem-tooltip></kendo:stockChart-navigator-seriesItem-tooltip>
    </kendo:stockChart-navigator-seriesItem>


## Configuration Attributes


### background `String`

The background color of the tooltip. The default is determined from the series color.

#### Example
    <kendo:stockChart background="background">
    </kendo:stockChart>



### color `String`

The text color of the tooltip. The default is the same as the series labels color.

#### Example
    <kendo:stockChart color="color">
    </kendo:stockChart>



### font `String`

The tooltip font.

#### Example
    <kendo:stockChart font="font">
    </kendo:stockChart>



### format `String`

The tooltip format.

#### Example
    <kendo:stockChart format="format">
    </kendo:stockChart>



### visible `boolean`

A value indicating if the tooltip should be displayed.

#### Example
    <kendo:stockChart visible="visible">
    </kendo:stockChart>



### template `Object`

The tooltip template.
Template variables:

#### Example
    <kendo:stockChart-navigator-seriesItem-tooltip template="template">
    </kendo:stockChart-navigator-seriesItem-tooltip>



### padding `Object`

The padding of the tooltip.

#### Example
    <kendo:stockChart-navigator-seriesItem-tooltip padding="padding">
    </kendo:stockChart-navigator-seriesItem-tooltip>



## Child JSP Tags

### kendo:stockChart-navigator-seriesItem-tooltip-border

The border configuration options.

More documentation is available at [kendo:stockChart-navigator-seriesItem-tooltip-border](/api/wrappers/jsp/stockchart/navigator-seriesitem-tooltip-border).

#### Example

    <kendo:stockChart-navigator-seriesItem-tooltip>
        <kendo:stockChart-navigator-seriesItem-tooltip-border></kendo:stockChart-navigator-seriesItem-tooltip-border>
    </kendo:stockChart-navigator-seriesItem-tooltip>
 