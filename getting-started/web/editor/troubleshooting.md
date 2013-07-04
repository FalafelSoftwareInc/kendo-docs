---
title: Troubleshooting
meta_title: Troubleshooting of Kendo UI Editor widget
meta_description: How to deal with the troubleshooting of Editor UI widget.
slug: editor-troubleshooting
ordinal: 3
publish: true
---

# Editor troubleshooting

## Pasting content in the editor when using IE does not display anything
Pasting in the editor requires permission to access clipboard data. This may require users with strict security settings to add the site in the trusted sites zone, or to adjust their Internet options so that the "Allow Programmatic clipboard access" setting is set to either "Allowed" or "Prompt".

## Editor inside a popup is readonly in Firefox
Firefox cannot handle iframes properly when they are moved in the DOM. When an Editor will be used inside a popup, which moves elements in the DOM, the popup (e.g. Kendo UI Window, jQuery dialog, etc) should be initialized first.
