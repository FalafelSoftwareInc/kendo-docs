---
title: Image Browser
slug: gs-web-editor-imagebrowser
tags: editor,imagebrowser,web
ordinal: 2
publish: true
---

# Image Browser

## Introduction

By default the "Insert Image" tool opens a simple dialog which allows the user to type in or paste the URL of an image and optionally specify a tooltip.

![Insert Image Dialog](editor-insert-image.png)

Since the Q3 2012 release KendoUI Editor widget supports a new way of picking an image by browsing a list of predefined files and directories. Uploading new images is also supported.

![Image Browser Dialog](editor-image-browser.png)

The image browser needs a server side implementation to retrieve and upload the files and directories.

## Configuring the ImageBrowser

The image browser tool can be configured through the [`imagebrowser` configuration option](/api/web/editor#imagebrowser).

#### Example

       $(document).ready(function(){
         $("#editor").kendoEditor({
             imageBrowser: {
                transport: {
                    read: "imagebrowser/read",
                    destroy: "imagebrowser/destroy",
                    create: "imagebrowser/createDirectory",
                    uploadUrl: "imagebrowser/upload",
                    thumbnailUrl: "imagebrowser/thumbnail"
                    imageUrl: "/content/images/{0}"
                }
             }
         });
      });
