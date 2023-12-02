

# \<track\>: The Embed Text Track element



::: section-content
The `<track>` [HTML](../index) element is used as a child of the media
elements, [`<audio>`](audio) and [`<video>`](video). It lets you specify
timed text tracks (or time-based data), for example to automatically
handle subtitles. The tracks are formatted in [WebVTT
format](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)
(`.vtt` files) --- Web Video Text Tracks.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<track\> {#html-demo-track .output-heading}

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
    <video controls src="/media/cc0-videos/friday.mp4">
      <track default kind="captions" srclang="en" src="/media/examples/friday.vtt" />
      Download the
      <a href="/media/cc0-videos/friday.mp4">MP4</a>
      video, and
      <a href="/media/examples/friday.vtt">subtitles</a>.
    </video>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    video {
      width: 250px;
    }

    video::cue {
      font-size: 1rem;
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

<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td>None</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>None; it is a <a
href="https://developer.mozilla.org/en-US/docs/Glossary/Void_element">void
element</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>As it is a void element, the start tag must be present and the end
tag must not be present.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td><p>A media element, <a href="audio"><code>&lt;audio&gt;</code></a>
or <a href="video"><code>&lt;video&gt;</code></a>.</p></td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a href="https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role"
target="_blank">No corresponding role</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>No <code>role</code> permitted</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLTrackElement"><code>HTMLTrackElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`default`](#default)

:   This attribute indicates that the track should be enabled unless the
    user\'s preferences indicate that another track is more appropriate.
    This may only be used on one `track` element per media element.

[`kind`](#kind)

:   How the text track is meant to be used. If omitted the default kind
    is `subtitles`. If the attribute contains an invalid value, it will
    use `metadata` (Versions of Chrome earlier than 52 treated an
    invalid value as `subtitles`). The following keywords are allowed:

    -   `subtitles`
        -   Subtitles provide translation of content that cannot be
            understood by the viewer. For example speech or text that is
            not English in an English language film.
        -   Subtitles may contain additional content, usually extra
            background information. For example the text at the
            beginning of the Star Wars films, or the date, time, and
            location of a scene.
    -   `captions`
        -   Closed captions provide a transcription and possibly a
            translation of audio.
        -   It may include important non-verbal information such as
            music cues or sound effects. It may indicate the cue\'s
            source (e.g. music, text, character).
        -   Suitable for users who are deaf or when the sound is muted.
    -   `descriptions`
        -   Textual description of the video content.
        -   Suitable for users who are blind or where the video cannot
            be seen.
    -   `chapters`
        -   Chapter titles are intended to be used when the user is
            navigating the media resource.
    -   `metadata`
        -   Tracks used by scripts. Not visible to the user.

[`label`](#label)

:   A user-readable title of the text track which is used by the browser
    when listing available text tracks.

[`src`](#src)

:   Address of the track (`.vtt` file). Must be a valid URL. This
    attribute must be specified and its URL value must have the same
    origin as the document --- unless the [`<audio>`](audio) or
    [`<video>`](video) parent element of the `track` element has a
    [`crossorigin`](../attributes/crossorigin) attribute.

[`srclang`](#srclang)

:   Language of the track text data. It must be a valid [BCP
    47](https://r12a.github.io/app-subtags/){target="_blank"} language
    tag. If the `kind` attribute is set to `subtitles`, then `srclang`
    must be defined.
:::

## Usage notes {#usage_notes}

### Track data types {#track_data_types}

::: section-content
The type of data that `track` adds to the media is set in the `kind`
attribute, which can take values of `subtitles`, `captions`,
`descriptions`, `chapters` or `metadata`. The element points to a source
file containing timed text that the browser exposes when the user
requests additional data.

A media element cannot have more than one `track` with the same `kind`,
`srclang`, and `label`.
:::

### Detecting cue changes {#detecting_cue_changes}

::: section-content
The underlying
[`TextTrack`](https://developer.mozilla.org/en-US/docs/Web/API/TextTrack),
indicated by the [`track`]{.page-not-created} property, receives a
`cuechange` event every time the currently-presented cue is changed.
This happens even if the track isn\'t associated with a media element.

If the track *is* associated with a media element, using the
[`<track>`](track){aria-current="page"} element as a child of the
[`<audio>`](audio) or [`<video>`](video) element, the `cuechange` event
is also sent to the
[`HTMLTrackElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLTrackElement).

::: code-example
[js]{.language-name}

``` {signature="67EKowfAlq7TgNHfEdB8agM11XlfU8ZhSWymmTwPLKs=" data-language="js"}
let textTrackElem = document.getElementById("texttrack");

textTrackElem.addEventListener("cuechange", (event) => {
  let cues = event.target.track.activeCues;
});
```
:::
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="bKQXYBuqH7YaVmBlgHrYOrXmYVHrlUhDCPQIWXo0ykg=" data-language="html"}
<video controls poster="/images/sample.gif">
  <source src="sample.mp4" type="video/mp4" />
  <source src="sample.ogv" type="video/ogv" />
  <track kind="captions" src="sampleCaptions.vtt" srclang="en" />
  <track kind="descriptions" src="sampleDescriptions.vtt" srclang="en" />
  <track kind="chapters" src="sampleChapters.vtt" srclang="en" />
  <track kind="subtitles" src="sampleSubtitles_de.vtt" srclang="de" />
  <track kind="subtitles" src="sampleSubtitles_en.vtt" srclang="en" />
  <track kind="subtitles" src="sampleSubtitles_ja.vtt" srclang="ja" />
  <track kind="subtitles" src="sampleSubtitles_oz.vtt" srclang="oz" />
  <track kind="metadata" src="keyStage1.vtt" srclang="en" label="Key Stage 1" />
  <track kind="metadata" src="keyStage2.vtt" srclang="en" label="Key Stage 2" />
  <track kind="metadata" src="keyStage3.vtt" srclang="en" label="Key Stage 3" />
  <!-- Fallback -->
  …
</video>
```
:::
:::

## Specifications

::: _table
  --------------------------------------------------------------------------------------------------
  Specification
  --------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-track-element]{.small}](https://html.spec.whatwg.org/multipage/media.html#the-track-element)

  --------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  --------------------------------------------------------------------------------------------------------------------------------------
              Desktop                                                Mobile                                                 
  ----------- --------- ------ --------- ---------- ------- -------- ------------ ------------ --------- --------- -------- ------------
              Chrome    Edge   Firefox   Internet   Opera   Safari   WebView      Chrome       Firefox   Opera     Safari   Samsung
                                         Explorer                    Android      Android      for       Android   on IOS   Internet
                                                                                               Android                      

  `track`     23        12     31        10         12.1    6        4.4          25           31        12.1      6        1.5
                                                                                                                            
                                                                     Doesn\'t     Doesn\'t                                  Doesn\'t
                                                                     work for     work for                                  work for
                                                                     fullscreen   fullscreen                                fullscreen
                                                                     video.       video.                                    video.

  `default`   23        12     31        10         12.1    6        4.4          25           31        12.1      6        1.5

  `kind`      23        12     31        10         12.1    6        4.4          25           31        14        6        1.5

  `label`     23        12     31        10         12.1    6        4.4          25           31        14        6        1.5

  `src`       23        12     31        10         12.1    6        4.4          25           31        14        6        1.5

  `srclang`   23        12     31        10         12.1    6        4.4          25           31        14        6        1.5
  --------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [WebVTT text track
    format](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)
-   [`HTMLMediaElement.textTracks`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/textTracks)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/track](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/track){._attribution-link}
:::
