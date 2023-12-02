

# HTML attribute: capture



::: section-content
The `capture` attribute specifies that, optionally, a new file should be
captured, and which device should be used to capture that new media of a
type defined by the [`accept`](accept) attribute.

Values include `user` and `environment`. The capture attribute is
supported on the [file](../element/input/file) input type.

The `capture` attribute takes as its value a string that specifies which
camera to use for capture of image or video data, if the
[accept](accept) attribute indicates that the input should be of one of
those types.

<figure class="table-container">
<div class="_table">
<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><code>user</code></td>
<td>The user-facing camera and/or microphone should be used.</td>
</tr>
<tr class="even">
<td><code>environment</code></td>
<td>The outward-facing camera and/or microphone should be used</td>
</tr>
</tbody>
</table>

</figure>

::: {#sect1 .notecard .note}
**Note:** Capture was previously a Boolean attribute which, if present,
requested that the device\'s media capture device(s) such as camera or
microphone be used instead of requesting a file input.
:::
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: capture {#html-demo-capture .output-heading}

Reset
:::

::: {#warning-no-script .warning-container}
::: warning
The interactive example cannot be shown because JavaScript is disabled.
:::
:::

::: {#warning-mathml-not-supported .warning-container .hidden}
::: warning
The interactive example cannot be shown because MathML is not supported
by your browser.
:::
:::

::: {#editor-container .editor-container .tabbed-standard .hidden .border-rounded-bottom editor-type="tabbed"}
::: {#tab-container .section .tabs}
::: {#tablist .tab-list role="tablist"}
HTML

CSS

JavaScript
:::

::: {#html-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="html" aria-hidden="true"}
::: {#html-editor}
    <label for="picture">Take a picture of your face:</label>

    <input type="file" name="picture" accept="image/*" capture="user" />

    <label for="voice">Record a sample of your voice:</label>

    <input type="file" name="voice" accept="audio/*" capture />
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    label {
      display: block;
      margin-top: 1rem;
    }

    input {
      margin-bottom: 1rem;
    }
:::
:::

::: {#js-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="js" aria-hidden="true"}
::: {#js-editor}
:::
:::
:::

::: {#output .output-container}
#### Output {.output-label}
:::
:::

::: {.section .console-container .hidden aria-hidden="true"}
#### Console Output {#console-output .console-label}

![]
clear console

::: {#console .console}
:::
:::

::: {#html-output .output .editor-tabbed}
%html-content%
:::
:::
:::

## Examples

::: section-content
When set on a file input type, operating systems with microphones and
cameras will display a user interface allowing the selection from an
existing file or the creating of a new one.

::: code-example
[html]{.language-name}

``` {signature="AUc+/evJbN5THWxxxjQg2zgx0EVtDbc8piVRFUZ/dY0=" data-language="html"}
<p>
  <label for="soundFile">What does your voice sound like?:</label>
  <input type="file" id="soundFile" capture="user" accept="audio/*" />
</p>
<p>
  <label for="videoFile">Upload a video:</label>
  <input type="file" id="videoFile" capture="environment" accept="video/*" />
</p>
<p>
  <label for="imageFile">Upload a photo of yourself:</label>
  <input type="file" id="imageFile" capture="user" accept="image/*" />
</p>
```
:::

::: {#sect2 .code-example}
::: iframe
:::
:::

Note these work better on mobile devices; if your device is a desktop
computer, you\'ll likely get a typical file picker.
:::

## Specifications

::: _table
  ------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------
  [HTML Media Capture\
  [\#
  dfn-capture]{.small}](https://w3c.github.io/html-media-capture/#dfn-capture)

  ------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
              Desktop                                                         Mobile                                                                                   
  ----------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
              Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `capture`   No        No     No        No                  No      No       4.4               25               79                    14              10              1.5
:::

## See also {#see_also}

::: section-content
-   [Using files from web
    applications](https://developer.mozilla.org/en-US/docs/Web/API/File_API/Using_files_from_web_applications)
-   [File API](https://developer.mozilla.org/en-US/docs/Web/API/File)
-   [`HTMLInputElement.files`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement/files)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/capture](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/capture){._attribution-link}
:::
