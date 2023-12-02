

# HTML attribute: accept



::: section-content
The `accept` attribute takes as its value a comma-separated list of one
or more file types, or [unique file type
specifiers](#unique_file_type_specifiers), describing which file types
to allow.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: accept {#html-demo-accept .output-heading}

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

::: {#editor-container .editor-container .tabbed-shorter .hidden .border-rounded-bottom editor-type="tabbed"}
::: {#tab-container .section .tabs}
::: {#tablist .tab-list role="tablist"}
HTML

CSS

JavaScript
:::

::: {#html-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="html" aria-hidden="true"}
::: {#html-editor}
    <label for="movie">Choose a movie to upload:</label>

    <input type="file" name="movie" accept="video/*" />

    <label for="poster">Choose a poster:</label>

    <input type="file" name="poster" accept="image/png, image/jpeg" />
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

## Overview

::: section-content
The accept property is an attribute of the [file](../element/input/file)
[`<input>`](../element/input) type. It was supported on the
[`<form>`](../element/form) element, but was removed in favor of
[file](../element/input/file).

Because a given file type may be identified in more than one manner,
it\'s useful to provide a thorough set of type specifiers when you need
files of specific type, or use the wild card to denote a type of any
format is acceptable.

For instance, there are a number of ways Microsoft Word files can be
identified, so a site that accepts Word files might use an `<input>`
like this:

::: code-example
[html]{.language-name}

``` {signature="VowkInl5TqdMjEIRHbdCVcl9oRwha/DRyTLFyyL0Faw=" data-language="html"}
<input
  type="file"
  id="docpicker"
  accept=".doc,.docx,application/msword,application/vnd.openxmlformats-officedocument.wordprocessingml.document" />
```
:::

Whereas if you\'re accepting a media file, you may want to be include
any format of that media type:

::: code-example
[html]{.language-name}

``` {signature="pY4M+8wxJ27U9qey55XdBtR84UaAwzvkTefKVXtgDi8=" data-language="html"}
<input type="file" id="soundFile" accept="audio/*" />
<input type="file" id="videoFile" accept="video/*" />
<input type="file" id="imageFile" accept="image/*" />
```
:::

The `accept` attribute doesn\'t validate the types of the selected
files; it provides hints for browsers to guide users towards selecting
the correct file types. It is still possible (in most cases) for users
to toggle an option in the file chooser that makes it possible to
override this and select any file they wish, and then choose incorrect
file types.

Because of this, you should make sure that expected requirement is
validated server-side.
:::

## Examples

::: section-content
When set on a file input type, the native file picker that opens up
should only enable selecting files of the correct file type. Most
operating systems lighten the files that don\'t match the criteria and
aren\'t selectable.

::: code-example
[html]{.language-name}

``` {signature="Fhu0seVLMmzLXLzMTk6LLMfRgTEYE22+EKIX7Grjfow=" data-language="html"}
<p>
  <label for="soundFile">Select an audio file:</label>
  <input type="file" id="soundFile" accept="audio/*" />
</p>
<p>
  <label for="videoFile">Select a video file:</label>
  <input type="file" id="videoFile" accept="video/*" />
</p>
<p>
  <label for="imageFile">Select some images:</label>
  <input type="file" id="imageFile" accept="image/*" multiple />
</p>
```
:::

::: {#sect1 .code-example}
::: iframe
:::
:::

Note the last example allows you to select multiple images. See the
[`multiple`](multiple) attribute for more information.
:::

## Unique file type specifiers {#unique_file_type_specifiers}

::: section-content
A **unique file type specifier** is a string that describes a type of
file that may be selected by the user in an
[`<input>`](../element/input) element of type `file`. Each unique file
type specifier may take one of the following forms:

-   A valid case-insensitive filename extension, starting with a period
    (\".\") character. For example: `.jpg`, `.pdf`, or `.doc`.
-   A valid MIME type string, with no extensions.
-   The string `audio/*` meaning \"any audio file\".
-   The string `video/*` meaning \"any video file\".
-   The string `image/*` meaning \"any image file\".

The `accept` attribute takes as its value a string containing one or
more of these unique file type specifiers, separated by commas. For
example, a file picker that needs content that can be presented as an
image, including both standard image formats and PDF files, might look
like this:

::: code-example
[html]{.language-name}

``` {signature="vaXAnYa80YDd/ePiItp1UmN0zsKPqN0izC31G0hsyIg=" data-language="html"}
<input type="file" accept="image/*,.pdf" />
```
:::
:::

## Using file inputs {#using_file_inputs}

### A basic example {#a_basic_example}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="F/T1yJHvhAVwkARDAgYCgjkZ4KzGemRGO90oG0vofHE=" data-language="html"}
<form method="post" enctype="multipart/form-data">
  
    <label for="file">Choose file to upload</label>
    <input type="file" id="file" name="file" multiple />
  
  
    <button>Submit</button>
  
</form>
```
:::

This produces the following output:

::: {#sect2 .code-example}
::: iframe
:::
:::

::: {#sect3 .notecard .note}
**Note:** You can find this example on GitHub too --- see the [source
code](https://github.com/mdn/learning-area/blob/main/html/forms/file-examples/simple-file.html){target="_blank"},
and also [see it running
live](https://mdn.github.io/learning-area/html/forms/file-examples/simple-file.html){target="_blank"}.
:::

Regardless of the user\'s device or operating system, the file input
provides a button that opens up a file picker dialog that allows the
user to choose a file.

Including the [`multiple`](multiple) attribute, as shown above,
specifies that multiple files can be chosen at once. The user can choose
multiple files from the file picker in any way that their chosen
platform allows (e.g. by holding down [Shift]{.kbd} or [Control]{.kbd},
and then clicking). If you only want the user to choose a single file
per `<input>`, omit the `multiple` attribute.
:::

### Limiting accepted file types {#limiting_accepted_file_types}

::: section-content
Often you won\'t want the user to be able to pick any arbitrary type of
file; instead, you often want them to select files of a specific type or
types. For example, if your file input lets users upload a profile
picture, you probably want them to select web-compatible image formats,
such as [JPEG](https://developer.mozilla.org/en-US/docs/Glossary/JPEG)
or [PNG](https://developer.mozilla.org/en-US/docs/Glossary/PNG).

Acceptable file types can be specified with the
[`accept`](../element/input/file#accept) attribute, which takes a
comma-separated list of allowed file extensions or MIME types. Some
examples:

-   `accept="image/png"` or `accept=".png"` --- Accepts PNG files.
-   `accept="image/png, image/jpeg"` or `accept=".png, .jpg, .jpeg"` ---
    Accept PNG or JPEG files.
-   `accept="image/*"` --- Accept any file with an `image/*` MIME type.
    (Many mobile devices also let the user take a picture with the
    camera when this is used.)
-   `accept=".doc,.docx,.xml,application/msword,application/vnd.openxmlformats-officedocument.wordprocessingml.document"`
    --- accept anything that smells like an MS Word document.

Let\'s look at a more complete example:

::: code-example
[html]{.language-name}

``` {signature="sO1n56AipdPykkyYIzuTKOBrH9jWxWeWOgHs6OXK758=" data-language="html"}
<form method="post" enctype="multipart/form-data">
  
    <label for="profile_pic">Choose file to upload</label>
    <input
      type="file"
      id="profile_pic"
      name="profile_pic"
      accept=".jpg, .jpeg, .png" />
  
  
    <button>Submit</button>
  
</form>
```
:::

::: {#sect4 .code-example}
::: iframe
:::
:::
:::

## Specifications

::: _table
  --------------------------------------------------------------------------------------------------
  Specification
  --------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  attr-input-accept]{.small}](https://html.spec.whatwg.org/multipage/input.html#attr-input-accept)

  --------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
             Desktop                                                         Mobile                                                                                   
  ---------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
             Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `accept`   1         12     1         6                   ≤12.1   1        4.4               18               4                     ≤12.1           1               1.0
:::

## See also {#see_also}

::: section-content
-   [Using files from web
    applications](https://developer.mozilla.org/en-US/docs/Web/API/File_API/Using_files_from_web_applications)
-   [File API](https://developer.mozilla.org/en-US/docs/Web/API/File)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/accept](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/accept){._attribution-link}
:::
