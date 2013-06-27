---
title: Javascript Dependencies
meta_title: Javascript Dependencies
meta_description: A list of scripts that Kendo UI widgets require to work, detailed explanation about all JavaScript files
slug: gs-javascript-dependencies
publish: true
---

# JavaScript files used by Kendo UI

Every Kendo UI widget needs its JavaScript files to be included in order to work properly. This help topic lists the JavaScript files required by each widget.

## Combined Scripts

The following combined scripts are provided in order to simplify development and deployment.

*   **kendo.all.min.js** contains a minified version of all scripts (Web, DataViz and Mobile).

> **Important**: kendo.all.min.js is available in the Kendo UI Complete, Kendo UI Complete for ASP.NET MVC, Kendo UI Complete for JSP and Kendo UI Complete for PHP distributions. The contents of
**kendo.aspnetmvc.min.js** are **not** included in kendo.all.min.js - you need to include kendo.aspnetmvc.min.js in addition to kendo.all.min.js or use the
[custom download builder tool](http://www.kendoui.com/custom-download).

*   **kendo.web.min.js** contains a minified version of all scripts from Kendo UI Web.
*   **kendo.dataviz.min.js** contains a minified version of all scripts from Kendo UI DataViz.
*   **kendo.mobile.min.js** contains a minified version of all scripts from Kendo UI Mobile.

> **Important:** Only one of the **kendo.web.min.js**, **kendo.dataviz.min.js** and **kendo.mobile.min.js** JavaScript files can be included at a time. If widgets from
different Kendo UI suites are needed one can either use **kendo.all.min.js** or create a custom combined JavaSript file via the [custom download builder tool](http://www.kendoui.com/custom-download).

## Custom Combined Scripts

Users who own a commercial license can use the [custom download builder tool](http://www.kendoui.com/custom-download)
to create a single JavaScript file which contains only the required widgets and features.

## CDN

The minified versions of all JavaScript files are also available via CDN

    http://cdn.kendostatic.com/<version>/js/<filename>.min.js

**e.g.** `http://cdn.kendostatic.com/2012.2.710/js/kendo.all.min.js`

> **Important:** in order to use HTTPS, you need to directly access the CloudFront CDN

    https://da7xgjtj801h2.cloudfront.net/<version>/js/<filename>.min.js

## jQuery version

The current official version of Kendo UI requires **jQuery 1.9.1**. There are occasions in which a new jQuery version is released, which introduces breaking changes and is not compatible with existing Kendo UI versions.
In such cases we recommend using the previous jQuery version until the next official Kendo UI release that resolves the problems. We normally do not change the jQuery version that is shipped
with Kendo UI for service packs. We can do this for major releases. The following list provides compatibility information about previous major Kendo UI releases:

* Kendo UI 2013.1.319 (Q1 2013) - jQuery 1.9.1
* Kendo UI 2012.3.1114 (Q3 2012) - jQuery 1.8.2
* Kendo UI 2012.2.710 (Q2 2012) - jQuery 1.7.1
* Kendo UI 2012.1.322 (Q1 2012) - jQuery 1.7.1
* Kendo UI 2011.3.1129 (Q3 2011) - jQuery 1.7.1

There should be no problem to use another minor jQuery version instead of the specified above, e.g. 1.7.2 instead of 1.7.1.

## Script tag placement

There is a general recommendation to place `script` tags before the closing `body` tag, so that the scripts are loaded and executed after the HTML markup. The Kendo UI widget
initialization statements are executed in the document.ready event via a jQuery handler. This means that the jQuery must be registered before any Kendo UI initialization statements. When using
the pure client-side-only Kendo UI widgets one can control the initialization statements' placement, so the jQuery script file can be registered at the bottom of the page. The Kendo UI widgets'
server wrappers are self-initialized, which means that each initialization script is rendered right after the widget's HTML markup. In this case the Kendo UI scripts can still be registered
at the end of the page, but the jQuery script must be registered in the `body` before the first Kendo UI widget on the page, or in the page `head`.

## Individual scripts

If more granular control is required, the following script files, either minified or not,
can be included on a per-widget basis.

### AutoComplete

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.data.odata.js (if binding to OData)
1.  kendo.model.js (if binding to XML)
1.  kendo.data.xml.js (if binding to XML)
1.  kendo.data.js
1.  kendo.fx.js (optional for animation)
1.  kendo.popup.js
1.  kendo.list.js
1.  kendo.autocomplete.js

### BarCode

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.dataviz.core.js
1.  kendo.dataviz.vml.js
1.  kendo.dataviz.svg.js
1.  kendo.dataviz.barcode.js

### Calendar

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.fx.js (optional for animation)
1.  kendo.calendar.js

### Chart

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.data.odata.js (if binding to OData)
1.  kendo.data.xml.js (if binding to XML)
1.  kendo.data.js
1.  kendo.binder.js (if using MVVM)
1.  kendo.dataviz.core.js
1.  kendo.dataviz.vml.js
1.  kendo.dataviz.svg.js
1.  kendo.dataviz.themes.js
1.  kendo.dataviz.chart.js
1.  kendo.dataviz.chart.polar.js
1.  kendo.userevents.js

### ComboBox

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.data.odata.js (if binding to OData)
1.  kendo.model.js (if binding to XML)
1.  kendo.data.xml.js (if binding to XML)
1.  kendo.data.js
1.  kendo.fx.js (optional for animation)
1.  kendo.popup.js
1.  kendo.list.js
1.  kendo.combobox.js

### ColorPicker

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.fx.js (optional for animation)
1.  kendo.userevents.js
1.  kendo.popup.js
1.  kendo.draganddrop.js
1.  kendo.slider.js
1.  kendo.data.js (if using MVVM)
1.  kendo.binder.js (if using MVVM)
1.  kendo.colorpicker.js

### ColorPalette

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.userevents.js
1.  kendo.data.js (if using MVVM)
1.  kendo.binder.js (if using MVVM)
1.  kendo.colorpicker.js

### DataSource

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.data.odata.js (if binding to OData)
1.  kendo.model.js (if binding to XML or editing)
1.  kendo.data.xml.js (if binding to XML)
1.  kendo.data.js


### DatePicker

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.fx.js (optional for animation)
1.  kendo.popup.js
1.  kendo.calendar.js
1.  kendo.datepicker.js


### Drag and Drop

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.draganddrop.js


### DropDownList

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.data.odata.js (if binding to OData)
1.  kendo.model.js (if binding to XML)
1.  kendo.data.xml.js (if binding to XML)
1.  kendo.data.js
1.  kendo.fx.js (optional for animation)
1.  kendo.popup.js
1.  kendo.list.js
1.  kendo.dropdownlist.js


### Editor

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.data.js
1.  kendo.userevents.js
1.  kendo.upload.js (if imagebrowser is used)
1.  kendo.selectable.js (if imagebrowser is used)
1.  kendo.listview.js (if imagebrowser is used)
1.  kendo.imagebrowser.js (if imagebrowser is used)
1.  kendo.popup.js
1.  kendo.list.js
1.  kendo.dropdownlist.js
1.  kendo.combobox.js
1.  kendo.fx.js (optional for animation)
1.  kendo.draganddrop.js (if popups are draggable and/or resizable)
1.  kendo.window.js
1.  kendo.colorpicker.js
1.  kendo.editor.js

### FlatColorPicker

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.userevents.js
1.  kendo.draganddrop.js
1.  kendo.slider.js
1.  kendo.data.js (if using MVVM)
1.  kendo.binder.js (if using MVVM)
1.  kendo.colorpicker.js


### Gauge

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.data.js (if using MVVM)
1.  kendo.binder.js (if using MVVM)
1.  kendo.dataviz.core.js
1.  kendo.dataviz.vml.js
1.  kendo.dataviz.svg.js
1.  kendo.dataviz.gauge.js


### Grid

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.data.odata.js (if binding to OData)
1.  kendo.data.xml.js (if binding to XML)
1.  kendo.data.js
1.  kendo.fx.js (optional for animation)
1.  kendo.popup.js (if editing or filtering is enabled)
1.  kendo.list.js&nbsp;(if editing or filtering is enabled)
1.  kendo.calendar.js (if editing or filtering is enabled)
1.  kendo.datepicker.js (if editing or filtering is enabled)
1.  kendo.numerictextbox.js (if editing or filtering is enabled)
1.  kendo.validator.js (if editing is enabled)
1.  kendo.binder.js (if editing is enabled)
1.  kendo.dropdownlist.js (if filtering is enabled)
1.  kendo.filtermenu.js (if filtering is enabled)
1.  kendo.pager.js (if paging is enabled)
1.  kendo.sortable.js (if sorting is enabled)
1.  kendo.userevents.js (if grouping, resizing or reordering is enabled)
1.  kendo.draganddrop.js (if grouping, resizing or reordering is enabled)
1.  kendo.groupable.js (if grouping is enabled)
1.  kendo.editable.js (if editing is enabled)
1.  kendo.selectable.js (if selection is enabled)
1.  kendo.resizable.js (if resizing is enabled)
1.  kendo.reorderable.js (if reordering is enabled)
1.  kendo.grid.js


### ListView

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.data.odata.js (if binding to OData)
1.  kendo.data.xml.js (if binding to XML)
1.  kendo.data.js
1.  kendo.validator.js (if editing is enabled)
1.  kendo.binder.js (if editing is enabled)
1.  kendo.pager.js (if pager is used)
1.  kendo.editable.js (if editing is enabled)
1.  kendo.selectable.js (if selection is enabled)
1.  kendo.listview.js


### Menu

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.fx.js (optional for animation)
1.  kendo.popup.js
1.  kendo.menu.js


### MultiSelect

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.data.odata.js (if binding to OData)
1.  kendo.model.js (if binding to XML)
1.  kendo.data.xml.js (if binding to XML)
1.  kendo.data.js
1.  kendo.fx.js (optional for animation)
1.  kendo.popup.js
1.  kendo.list.js
1.  kendo.multiselect.js


### NumericTextBox

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.userevents.js
1.  kendo.numerictextbox.js

### PanelBar

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.fx.js (optional for animation)
1.  kendo.panelbar.js

### QRCode

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.dataviz.core.js
1.  kendo.dataviz.vml.js
1.  kendo.dataviz.svg.js
1.  kendo.dataviz.qrcode.js

### Slider and RangeSlider

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.userevents.js
1.  kendo.binder.js (if using MVVM)
1.  kendo.draganddrop.js
1.  kendo.slider.js

### Splitter

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.userevents.js
1.  kendo.draganddrop.js
1.  kendo.resizable.js
1.  kendo.splitter.js

### Sparkline

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.data.odata.js (if binding to OData)
1.  kendo.data.xml.js (if binding to XML)
1.  kendo.data.js
1.  kendo.userevents.js
1.  <span>kendo.binder.js (if using MVVM)</span>
1.  kendo.dataviz.core.js
1.  kendo.dataviz.vml.js
1.  kendo.dataviz.svg.js
1.  kendo.dataviz.themes.js
1.  kendo.dataviz.chart.js
1.  kendo.dataviz.sparkline.js

### StockChart

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.data.odata.js (if binding to OData)
1.  kendo.data.xml.js (if binding to XML)
1.  kendo.data.js
1.  kendo.userevents.js
1.  <span>kendo.binder.js (if using MVVM)</span>
1.  kendo.dataviz.core.js
1.  kendo.dataviz.vml.js
1.  kendo.dataviz.svg.js
1.  kendo.dataviz.themes.js
1.  kendo.dataviz.chart.js
1.  kendo.dataviz.stock.js

### TabStrip

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.data.js
1.  kendo.fx.js (optional for animation)
1.  kendo.tabstrip.js


### TimePicker

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.fx.js (optional for animation)
1.  kendo.popup.js
1.  kendo.timepicker.js

### Tooltip

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.fx.js (optional for animation)
1.  kendo.popup.js
1.  kendo.tooltip.js

### TreeView

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.userevents.js
1.  kendo.data.js
1.  kendo.fx.js (optional for animation)
1.  kendo.draganddrop.js (if drag &amp; drop enabled)
1.  kendo.treeview.js


### Upload

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.upload.js


### Validator

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.validator.js


### Window

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.userevents.js
1.  kendo.fx.js (optional for animation)
1.  kendo.draganddrop.js
1.  kendo.resizable.js
1.  kendo.window.js


### Mobile Application

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.history.js
1.  kendo.fx.js
1.  kendo.draganddrop.js
1.  kendo.mobile.scroller.js
1.  kendo.mobile.view.js
1.  kendo.mobile.pane.js
1.  kendo.mobile.application.js

### Mobile ActionSheet

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.history.js
1.  kendo.popup.js
1.  kendo.fx.js
1.  kendo.draganddrop.js
1.  kendo.mobile.shim.js
1.  kendo.mobile.scroller.js
1.  kendo.mobile.view.js
1.  kendo.mobile.pane.js
1.  kendo.mobile.application.js
1.  kendo.mobile.actionsheet.js


### Mobile Button

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.history.js
1.  kendo.fx.js
1.  kendo.draganddrop.js
1.  kendo.mobile.scroller.js
1.  kendo.mobile.view.js
1.  kendo.mobile.pane.js
1.  kendo.mobile.application.js
1.  kendo.mobile.button.js


### Mobile ButtonGroup

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.history.js
1.  kendo.fx.js
1.  kendo.draganddrop.js
1.  kendo.mobile.scroller.js
1.  kendo.mobile.view.js
1.  kendo.mobile.pane.js
1.  kendo.mobile.application.js
1.  kendo.mobile.buttongroup.js


### Mobile ListView

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.data.js
1.  kendo.data.odata.js
1.  kendo.data.xml.js
1.  kendo.model.js
1.  kendo.history.js
1.  kendo.fx.js
1.  kendo.draganddrop.js
1.  kendo.mobile.scroller.js
1.  kendo.mobile.view.js
1.  kendo.mobile.pane.js
1.  kendo.mobile.application.js
1.  kendo.mobile.listview.js

### Mobile ModalView

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.popup.js
1.  kendo.history.js
1.  kendo.fx.js
1.  kendo.draganddrop.js
1.  kendo.mobile.shim.js
1.  kendo.mobile.scroller.js
1.  kendo.mobile.view.js
1.  kendo.mobile.pane.js
1.  kendo.mobile.application.js
1.  kendo.mobile.modalview.js

### Mobile NavBar

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.history.js
1.  kendo.fx.js
1.  kendo.draganddrop.js
1.  kendo.mobile.scroller.js
1.  kendo.mobile.view.js
1.  kendo.mobile.pane.js
1.  kendo.mobile.application.js
1.  kendo.mobile.navbar.js

### Mobile PopOver

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.popup.js
1.  kendo.history.js
1.  kendo.fx.js
1.  kendo.draganddrop.js
1.  kendo.mobile.shim.js
1.  kendo.mobile.scroller.js
1.  kendo.mobile.view.js
1.  kendo.mobile.pane.js
1.  kendo.mobile.application.js
1.  kendo.mobile.popover.js

### Mobile Scroller

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.history.js
1.  kendo.fx.js
1.  kendo.draganddrop.js
1.  kendo.mobile.scroller.js


### Mobile ScrollView

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.history.js
1.  kendo.fx.js
1.  kendo.draganddrop.js
1.  kendo.mobile.scroller.js
1.  kendo.mobile.view.js
1.  kendo.mobile.pane.js
1.  kendo.mobile.application.js
1.  kendo.mobile.scrollview.js

### Mobile SplitView

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.history.js
1.  kendo.fx.js
1.  kendo.draganddrop.js
1.  kendo.mobile.scroller.js
1.  kendo.mobile.view.js
1.  kendo.mobile.pane.js
1.  kendo.mobile.application.js
1.  kendo.mobile.splitview.js


### Mobile Switch

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.history.js
1.  kendo.fx.js
1.  kendo.draganddrop.js
1.  kendo.mobile.scroller.js
1.  kendo.mobile.view.js
1.  kendo.mobile.pane.js
1.  kendo.mobile.application.js
1.  kendo.mobile.switch.js


### Mobile TabStrip

1.  jquery-1.9.1.js
1.  kendo.core.js
1.  kendo.history.js
1.  kendo.fx.js
1.  kendo.draganddrop.js
1.  kendo.mobile.scroller.js
1.  kendo.mobile.view.js
1.  kendo.mobile.pane.js
1.  kendo.mobile.application.js
1.  kendo.mobile.tabstrip.js

