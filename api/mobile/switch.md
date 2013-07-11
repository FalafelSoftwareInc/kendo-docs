---
title: kendo.mobile.ui.Switch
meta_title: Configuration, methods and events of Kendo UI Mobile Switch
meta_description: How to quickly configure the checked and unchecked state of Mobile Switch widget.
slug: api-mobile-switch
relatedDocs: gs-mobile-switch
tags: api,mobile
publish: true
---

# kendo.mobile.ui.Switch

Represents the Kendo UI Mobile Switch widget. Inherits from [kendo.mobile.ui.Widget](/api/framework/mobilewidget).

## Configuration

### checked `Boolean`*(default: false)*

 The checked state of the widget.

### offLabel `String`*(default: "OFF")*

 The OFF label.

### onLabel `String`*(default: "ON")*

 The ON label.

## Methods

### check

Get/Set the checked state of the widget.

#### Example

    <input data-role="switch" id="foo" />;

    <script>
      // get a reference to the switch widget
      var switchInstance = $("#foo").data("kendoMobileSwitch");

      // get the checked state of the switch.
      var checked = switchInstance.check();

      // set the checked state of the switch.
      switchInstance.check(true);
    </script>

#### Parameters

##### check `Boolean`

Whether to turn the widget on or off.

#### Returns

`Boolean` The checked state of the widget.

### destroy
Prepares the **Switch** for safe removal from DOM. Detaches all event handlers and removes jQuery.data attributes to avoid memory leaks. Calls destroy method of any child Kendo widgets.

> **Important:** This method does not remove the Switch element from DOM.

#### Example

    var switchInstance = $("#switch").data("kendoMobileSwitch");

    // detach events
    switchInstance.destroy();

### toggle

Toggle the checked state of the widget.

#### Example

    <input data-role="switch" id="foo" />;

    <script>
      // get a reference to the switch
      var switchInstance = $("#foo").data("kendoMobileSwitch");

      // toggle the checked state of the switch.
      switchInstance.toggle();
    </script>

## Events

### change

Fires when the state of the widget changes

#### Handle mobile Switch change event

    <input type="checkbox" id="switch" data-role="switch" />

    <script>
     $("#switch").data("kendoMobileSwitch").bind("change", function(e) {
         console.log(e.checked); // true or false
     }
    </script>

#### Event Data

##### e.checked `Object`

The checked state of the widget.
