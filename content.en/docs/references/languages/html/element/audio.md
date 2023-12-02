

# \<audio\>: The Embed Audio element



::: section-content
The `<audio>` [HTML](../index) element is used to embed sound content in
documents. It may contain one or more audio sources, represented using
the `src` attribute or the [`<source>`](source) element: the browser
will choose the most suitable one. It can also be the destination for
streamed media, using a
[`MediaStream`](https://developer.mozilla.org/en-US/docs/Web/API/MediaStream).
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<audio\> {#html-demo-audio .output-heading}

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
    <figure>
      <figcaption>Listen to the T-Rex:</figcaption>
      <audio controls src="/media/cc0-audio/t-rex-roar.mp3">
        <a href="/media/cc0-audio/t-rex-roar.mp3"> Download audio </a>
      </audio>
    </figure>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    figure {
      margin: 0;
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

The above example shows simple usage of the `<audio>` element. In a
similar manner to the [`<img>`](img) element, we include a path to the
media we want to embed inside the `src` attribute; we can include other
attributes to specify information such as whether we want it to autoplay
and loop, whether we want to show the browser\'s default audio controls,
etc.

The content inside the opening and closing `<audio></audio>` tags is
shown as a fallback in browsers that don\'t support the element.
:::

## Attributes

::: section-content
This element\'s attributes include the [global
attributes](../global_attributes).

[`autoplay`](#autoplay)

:   A Boolean attribute: if specified, the audio will automatically
    begin playback as soon as it can do so, without waiting for the
    entire audio file to finish downloading.

    ::: {#sect1 .notecard .note}
    **Note:** Sites that automatically play audio (or videos with an
    audio track) can be an unpleasant experience for users, so should be
    avoided when possible. If you must offer autoplay functionality, you
    should make it opt-in (requiring a user to specifically enable it).
    However, this can be useful when creating media elements whose
    source will be set at a later time, under user control. See our
    [autoplay
    guide](https://developer.mozilla.org/en-US/docs/Web/Media/Autoplay_guide)
    for additional information about how to properly use autoplay.
    :::

[`controls`](#controls)

:   If this attribute is present, the browser will offer controls to
    allow the user to control audio playback, including volume, seeking,
    and pause/resume playback.

[`controlslist`](#controlslist) [Experimental]{.visually-hidden} [Non-standard]{.visually-hidden}

:   The
    [`controlslist`](https://wicg.github.io/controls-list/explainer.html){target="_blank"}
    attribute, when specified, helps the browser select what controls to
    show for the `audio` element whenever the browser shows its own set
    of controls (that is, when the `controls` attribute is specified).

    The allowed values are `nodownload`, `nofullscreen` and
    `noremoteplayback`.

[`crossorigin`](#crossorigin)

:   This
    [enumerated](https://developer.mozilla.org/en-US/docs/Glossary/Enumerated)
    attribute indicates whether to use CORS to fetch the related audio
    file. [CORS-enabled resources](../cors_enabled_image) can be reused
    in the [`<canvas>`](canvas) element without being *tainted*. The
    allowed values are:

    [`anonymous`](#anonymous)

    :   Sends a cross-origin request without a credential. In other
        words, it sends the `Origin:` HTTP header without a cookie,
        X.509 certificate, or performing HTTP Basic authentication. If
        the server does not give credentials to the origin site (by not
        setting the `Access-Control-Allow-Origin:` HTTP header), the
        resource will be *tainted*, and its usage restricted.

    [`use-credentials`](#use-credentials)

    :   Sends a cross-origin request with a credential. In other words,
        it sends the `Origin:` HTTP header with a cookie, a certificate,
        or performing HTTP Basic authentication. If the server does not
        give credentials to the origin site (through
        `Access-Control-Allow-Credentials:` HTTP header), the resource
        will be *tainted* and its usage restricted.

    When not present, the resource is fetched without a CORS request
    (i.e. without sending the `Origin:` HTTP header), preventing its
    non-tainted use in [`<canvas>`](canvas) elements. If invalid, it is
    handled as if the enumerated keyword **anonymous** was used. See
    [CORS settings attributes](../attributes/crossorigin) for additional
    information.

[`disableremoteplayback`](#disableremoteplayback) [Experimental]{.visually-hidden}

:   A Boolean attribute used to disable the capability of remote
    playback in devices that are attached using wired (HDMI, DVI, etc.)
    and wireless technologies (Miracast, Chromecast, DLNA, AirPlay,
    etc.). See [this proposed
    specification](https://www.w3.org/TR/remote-playback/#the-disableremoteplayback-attribute){target="_blank"}
    for more information.

    ::: {#sect2 .notecard .note}
    **Note:** In Safari, you can use
    [`x-webkit-airplay="deny"`](https://developer.apple.com/library/archive/documentation/AudioVideo/Conceptual/AirPlayGuide/OptingInorOutofAirPlay/OptingInorOutofAirPlay.html){target="_blank"}
    as a fallback.
    :::

[`loop`](#loop)

:   A Boolean attribute: if specified, the audio player will
    automatically seek back to the start upon reaching the end of the
    audio.

[`muted`](#muted)

:   A Boolean attribute that indicates whether the audio will be
    initially silenced. Its default value is `false`.

[`preload`](#preload)

:   This
    [enumerated](https://developer.mozilla.org/en-US/docs/Glossary/Enumerated)
    attribute is intended to provide a hint to the browser about what
    the author thinks will lead to the best user experience. It may have
    one of the following values:

    -   `none`: Indicates that the audio should not be preloaded.
    -   `metadata`: Indicates that only audio metadata (e.g. length) is
        fetched.
    -   `auto`: Indicates that the whole audio file can be downloaded,
        even if the user is not expected to use it.
    -   *empty string*: A synonym of the `auto` value.

    The default value is different for each browser. The spec advises it
    to be set to `metadata`.

    ::: {#sect3 .notecard .note}
    **Note:**

    -   The `autoplay` attribute has precedence over `preload`. If
        `autoplay` is specified, the browser would obviously need to
        start downloading the audio for playback.
    -   The browser is not forced by the specification to follow the
        value of this attribute; it is a mere hint.
    :::

[`src`](#src)

:   The URL of the audio to embed. This is subject to [HTTP access
    controls](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS).
    This is optional; you may instead use the [`<source>`](source)
    element within the audio block to specify the audio to embed.
:::

## Events

::: section-content
<figure class="table-container">
<div class="_table">
<table class="no-markdown">
<thead>
<tr class="header">
<th scope="col">Event name</th>
<th scope="col">Fired when</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/ScriptProcessorNode/audioprocess_event"><code>audioprocess</code></a></td>
<td>The input buffer of a <a
href="https://developer.mozilla.org/en-US/docs/Web/API/ScriptProcessorNode"><code>ScriptProcessorNode</code></a>
is ready to be processed.</td>
</tr>
<tr class="even">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/canplay_event"><code>canplay</code></a></td>
<td>The browser can play the media, but estimates that not enough data
has been loaded to play the media up to its end without having to stop
for further buffering of content.</td>
</tr>
<tr class="odd">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/canplaythrough_event"><code>canplaythrough</code></a></td>
<td>The browser estimates it can play the media up to its end without
stopping for content buffering.</td>
</tr>
<tr class="even">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/OfflineAudioContext/complete_event"><code>complete</code></a></td>
<td>The rendering of an <a
href="https://developer.mozilla.org/en-US/docs/Web/API/OfflineAudioContext"><code>OfflineAudioContext</code></a>
is terminated.</td>
</tr>
<tr class="odd">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/durationchange_event"><code>durationchange</code></a></td>
<td>The <code>duration</code> attribute has been updated.</td>
</tr>
<tr class="even">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/emptied_event"><code>emptied</code></a></td>
<td>The media has become empty; for example, this event is sent if the
media has already been loaded (or partially loaded), and the <a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/load"><code>HTMLMediaElement.load</code></a>
method is called to reload it.</td>
</tr>
<tr class="odd">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/ended_event"><code>ended</code></a></td>
<td>Playback has stopped because the end of the media was reached.</td>
</tr>
<tr class="even">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/loadeddata_event"><code>loadeddata</code></a></td>
<td>The first frame of the media has finished loading.</td>
</tr>
<tr class="odd">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/loadedmetadata_event"><code>loadedmetadata</code></a></td>
<td>The metadata has been loaded.</td>
</tr>
<tr class="even">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/loadstart_event"><code>loadstart</code></a></td>
<td>Fired when the browser has started to load the resource.</td>
</tr>
<tr class="odd">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/pause_event"><code>pause</code></a></td>
<td>Playback has been paused.</td>
</tr>
<tr class="even">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/play_event"><code>play</code></a></td>
<td>Playback has begun.</td>
</tr>
<tr class="odd">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/playing_event"><code>playing</code></a></td>
<td>Playback is ready to start after having been paused or delayed due
to lack of data.</td>
</tr>
<tr class="even">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/ratechange_event"><code>ratechange</code></a></td>
<td>The playback rate has changed.</td>
</tr>
<tr class="odd">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/seeked_event"><code>seeked</code></a></td>
<td>A <em>seek</em> operation completed.</td>
</tr>
<tr class="even">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/seeking_event"><code>seeking</code></a></td>
<td>A <em>seek</em> operation began.</td>
</tr>
<tr class="odd">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/stalled_event"><code>stalled</code></a></td>
<td>The user agent is trying to fetch media data, but data is
unexpectedly not forthcoming.</td>
</tr>
<tr class="even">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/suspend_event"><code>suspend</code></a></td>
<td>Media data loading has been suspended.</td>
</tr>
<tr class="odd">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/timeupdate_event"><code>timeupdate</code></a></td>
<td>The time indicated by the <code>currentTime</code> attribute has
been updated.</td>
</tr>
<tr class="even">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/volumechange_event"><code>volumechange</code></a></td>
<td>The volume has changed.</td>
</tr>
<tr class="odd">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/waiting_event"><code>waiting</code></a></td>
<td>Playback has stopped because of a temporary lack of data</td>
</tr>
</tbody>
</table>

</figure>
:::

## Usage notes {#usage_notes}

::: section-content
Browsers don\'t all support the same [file
types](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Containers)
and [audio
codecs](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Audio_codecs);
you can provide multiple sources inside nested [`<source>`](source)
elements, and the browser will then use the first one it understands:

::: code-example
[html]{.language-name}

``` {signature="0CcgF3IhkgyeJhNAWnl5iF8K48gDwM5JZRmmQqH3pyg=" data-language="html"}
<audio controls>
  <source src="myAudio.mp3" type="audio/mpeg" />
  <source src="myAudio.ogg" type="audio/ogg" />
  <p>
    Download <a href="myAudio.mp3">MP3</a> or
    <a href="myAudio.ogg">OGG</a> audio.
  </p>
</audio>
```
:::

We offer a substantive and thorough [guide to media file
types](https://developer.mozilla.org/en-US/docs/Web/Media/Formats) and
the [audio codecs that can be used within
them](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Audio_codecs).
Also available is [a guide to the codecs supported for
video](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs).

Other usage notes:

-   If you don\'t specify the `controls` attribute, the audio player
    won\'t include the browser\'s default controls. You can, however,
    create your own custom controls using JavaScript and the
    [`HTMLMediaElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement)
    API.
-   To allow precise control over your audio content,
    `HTMLMediaElement`s fire many different
    [events](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement#events).
    This also provides a way to monitor the audio\'s fetching process so
    you can watch for errors or detect when enough is available to begin
    to play or manipulate it.
-   You can also use the [Web Audio
    API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API)
    to directly generate and manipulate audio streams from JavaScript
    code rather than streaming pre-existing audio files.
-   `<audio>` elements can\'t have subtitles or captions associated with
    them in the same way that `<video>` elements can. See [WebVTT and
    Audio](https://www.iandevlin.com/blog/2015/12/html5/webvtt-and-audio/){target="_blank"}
    by Ian Devlin for some useful information and workarounds.
-   To test the fallback content on browsers that support the element,
    you can replace `<audio>` with a non-existing element like
    `<notanaudio>`.

A good general source of information on using HTML `<audio>` is the
[Video and audio
content](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content)
beginner\'s tutorial.
:::

### Styling with CSS {#styling_with_css}

::: section-content
The `<audio>` element has no intrinsic visual output of its own unless
the `controls` attribute is specified, in which case the browser\'s
default controls are shown.

The default controls have a
[`display`](https://developer.mozilla.org/en-US/docs/Web/CSS/display)
value of `inline` by default, and it is often a good idea to set the
value to `block` to improve control over positioning and layout, unless
you want it to sit within a text block or similar.

You can style the default controls with properties that affect the block
as a single unit, so for example you can give it a
[`border`](https://developer.mozilla.org/en-US/docs/Web/CSS/border) and
[`border-radius`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius),
[`padding`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding),
[`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin),
etc. You can\'t however style the individual components inside the audio
player (e.g. change the button size or icons, change the font, etc.),
and the controls are different across the different browsers.

To get a consistent look and feel across browsers, you\'ll need to
create custom controls; these can be marked up and styled in whatever
way you want, and then JavaScript can be used along with the
[`HTMLMediaElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement)
API to wire up their functionality.

[Video player styling
basics](https://developer.mozilla.org/en-US/docs/Web/Guide/Audio_and_video_delivery/Video_player_styling_basics)
provides some useful styling techniques --- it is written in the context
of `<video>`, but much of it is equally applicable to `<audio>`.
:::

### Detecting addition and removal of tracks {#detecting_addition_and_removal_of_tracks}

::: section-content
You can detect when tracks are added to and removed from an `<audio>`
element using the
[`addtrack`](https://developer.mozilla.org/en-US/docs/Web/API/AudioTrackList/addtrack_event)
and
[`removetrack`](https://developer.mozilla.org/en-US/docs/Web/API/AudioTrackList/removetrack_event)
events. However, these events aren\'t sent directly to the `<audio>`
element itself. Instead, they\'re sent to the track list object within
the `<audio>` element\'s
[`HTMLMediaElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement)
that corresponds to the type of track that was added to the element:

[`HTMLMediaElement.audioTracks`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/audioTracks)

:   An
    [`AudioTrackList`](https://developer.mozilla.org/en-US/docs/Web/API/AudioTrackList)
    containing all of the media element\'s audio tracks. You can add a
    listener for `addtrack` to this object to be alerted when new audio
    tracks are added to the element.

[`HTMLMediaElement.videoTracks`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/videoTracks)

:   Add an `addtrack` listener to this
    [`VideoTrackList`](https://developer.mozilla.org/en-US/docs/Web/API/VideoTrackList)
    object to be informed when video tracks are added to the element.

[`HTMLMediaElement.textTracks`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/textTracks)

:   Add an `addtrack` event listener to this
    [`TextTrackList`](https://developer.mozilla.org/en-US/docs/Web/API/TextTrackList)
    to be notified when new text tracks are added to the element.

::: {#sect4 .notecard .note}
**Note:** Even though it\'s an `<audio>` element, it still has video and
text track lists, and can in fact be used to present video, although the
user interface implications can be odd.
:::

For example, to detect when audio tracks are added to or removed from an
`<audio>` element, you can use code like this:

::: code-example
[js]{.language-name}

``` {signature="WWiGUEghTsXZ5HGZpeipRfRlqQb1Vg6xl5KO4RlCap0=" data-language="js"}
const elem = document.querySelector("audio");

elem.audioTrackList.onaddtrack = (event) => {
  trackEditor.addTrack(event.track);
};

elem.audioTrackList.onremovetrack = (event) => {
  trackEditor.removeTrack(event.track);
};
```
:::

This code watches for audio tracks to be added to and removed from the
element, and calls a hypothetical function on a track editor to register
and remove the track from the editor\'s list of available tracks.

You can also use
[`addEventListener()`](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)
to listen for the
[`addtrack`](https://developer.mozilla.org/en-US/docs/Web/API/AudioTrackList/addtrack_event)
and
[`removetrack`](https://developer.mozilla.org/en-US/docs/Web/API/AudioTrackList/removetrack_event)
events.
:::

## Examples

### Basic usage {#basic_usage}

::: section-content
The following example shows simple usage of the `<audio>` element to
play an OGG file. It will autoplay due to the `autoplay` attribute---if
the page has permission to do so---and also includes fallback content.

::: code-example
[html]{.language-name}

``` {signature="J7wAAtooMS4sRzisPIzdU08hJiRPsY7/x2qfTDUp1nk=" data-language="html"}
<!-- Simple audio playback -->
<audio src="AudioTest.ogg" autoplay>
  <a href="AudioTest.ogg">Download OGG audio</a>.
</audio>
```
:::

For details on when autoplay works, how to get permission to use
autoplay, and how and when it\'s appropriate to use autoplay, see our
[autoplay
guide](https://developer.mozilla.org/en-US/docs/Web/Media/Autoplay_guide).
:::

### \<audio\> element with \<source\> element {#audio_element_with_source_element}

::: section-content
This example specifies which audio track to embed using the `src`
attribute on a nested `<source>` element rather than directly on the
`<audio>` element. It is always useful to include the file\'s MIME type
inside the `type` attribute, as the browser is able to instantly tell if
it can play that file, and not waste time on it if not.

::: code-example
[html]{.language-name}

``` {signature="64ehXs30CHk+gNBjXWiItEOdU+8psnMNVwaqMi0c1uc=" data-language="html"}
<audio controls>
  <source src="foo.wav" type="audio/wav" />
  <a href="foo.wav">Download WAV audio</a>.
</audio>
```
:::
:::

### \<audio\> with multiple \<source\> elements {#audio_with_multiple_source_elements}

::: section-content
This example includes multiple `<source>` elements. The browser tries to
load the first source element (Opus) if it is able to play it; if not it
falls back to the second (Vorbis) and finally back to MP3:

::: code-example
[html]{.language-name}

``` {signature="ObJgf9YgTgAfS0z7WJqzaIqVpHQ2SeadTF2BLNuXSX8=" data-language="html"}
<audio controls>
  <source src="foo.opus" type="audio/ogg; codecs=opus" />
  <source src="foo.ogg" type="audio/ogg; codecs=vorbis" />
  <source src="foo.mp3" type="audio/mpeg" />
</audio>
```
:::
:::

## Accessibility concerns {#accessibility_concerns}

::: section-content
Audio with spoken dialog should provide both captions and transcripts
that accurately describe its content. Captions, which are specified
using
[WebVTT](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API),
allow people who are hearing impaired to understand an audio
recording\'s content as the recording is being played, while transcripts
allow people who need additional time to be able to review the
recording\'s content at a pace and format that is comfortable for them.

If automatic captioning services are used, it is important to review the
generated content to ensure it accurately represents the source audio.

The `<audio>` element doesn\'t directly support WebVTT. You will have to
find a library or framework that provides the capability for you, or
write the code to display captions yourself. One option is to play your
audio using a [`<video>`](video) element, which does support WebVTT.

In addition to spoken dialog, subtitles and transcripts should also
identify music and sound effects that communicate important information.
This includes emotion and tone. For example, in the WebVTT below, note
the use of square brackets to provide tone and emotional insight to the
viewer; this can help establish the mood otherwise provided using music,
nonverbal sounds and crucial sound effects, and so forth.

``` {data-language="plain"}
1
00:00:00 --> 00:00:45
[Energetic techno music]

2
00:00:46 --> 00:00:51
Welcome to the Time Keeper's podcast! In this episode we're discussing which Swisswatch is a wrist switchwatch?

16
00:00:52 --> 00:01:02
[Laughing] Sorry! I mean, which wristwatch is a Swiss wristwatch?
```

Also it\'s a good practice to provide some content (such as the direct
download link) as a fallback for viewers who use a browser in which the
`<audio>` element is not supported:

::: code-example
[html]{.language-name}

``` {signature="0CcgF3IhkgyeJhNAWnl5iF8K48gDwM5JZRmmQqH3pyg=" data-language="html"}
<audio controls>
  <source src="myAudio.mp3" type="audio/mpeg" />
  <source src="myAudio.ogg" type="audio/ogg" />
  <p>
    Download <a href="myAudio.mp3">MP3</a> or
    <a href="myAudio.ogg">OGG</a> audio.
  </p>
</audio>
```
:::

-   [Web Video Text Tracks Format
    (WebVTT)](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)
-   [WebAIM: Captions, Transcripts, and Audio
    Descriptions](https://webaim.org/techniques/captions/){target="_blank"}
-   [MDN Understanding WCAG, Guideline 1.2
    explanations](https://developer.mozilla.org/en-US/docs/Web/Accessibility/Understanding_WCAG/Perceivable#guideline_1.2_%E2%80%94_providing_text_alternatives_for_time-based_media)
-   [Understanding Success Criterion 1.2.1 \| W3C Understanding WCAG
    2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/media-equiv-av-only-alt.html){target="_blank"}
-   [Understanding Success Criterion 1.2.2 \| W3C Understanding WCAG
    2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/media-equiv-captions.html){target="_blank"}
:::

## Technical summary {#technical_summary}

::: section-content
<figure class="table-container">
<div class="_table">
<table class="properties">
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td><a href="../content_categories#flow_content">Flow content</a>,
phrasing content, embedded content. If it has a <a href="audio#controls"
aria-current="page"><code>controls</code></a> attribute: interactive
content and palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>If the element has a <a href="audio#src"
aria-current="page"><code>src</code></a> attribute: zero or more <a
href="track"><code>&lt;track&gt;</code></a> elements followed by
transparent content that contains no <a href="audio"
aria-current="page"><code>&lt;audio&gt;</code></a> or <a
href="video"><code>&lt;video&gt;</code></a> media elements.<br />
Else: zero or more <a href="source"><code>&lt;source&gt;</code></a>
elements followed by zero or more <a
href="track"><code>&lt;track&gt;</code></a> elements followed by
transparent content that contains no <a href="audio"
aria-current="page"><code>&lt;audio&gt;</code></a> or <a
href="video"><code>&lt;video&gt;</code></a> media elements.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts embedded content.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a href="https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role"
target="_blank">No corresponding role</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/application_role"><code>application</code></a></td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLAudioElement"><code>HTMLAudioElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  --------------------------------------------------------------------------------------------------
  Specification
  --------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-audio-element]{.small}](https://html.spec.whatwg.org/multipage/media.html#the-audio-element)

  --------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  --------------------------------------------------------------------------------------------------------------------------------------------------
               Desktop                                                        Mobile                                                    
  ------------ ------------ ------ --------- ---------- ------------ -------- ------------ ------------ --------- ------------ -------- ------------
               Chrome       Edge   Firefox   Internet   Opera        Safari   WebView      Chrome       Firefox   Opera        Safari   Samsung
                                             Explorer                         Android      Android      for       Android      on IOS   Internet
                                                                                                        Android                         

  `audio`      3            12     3.5       9          10.5         3.1      3            18           4         11           3        1.0
                                                                                                                                        
                                   For                                                                  For                             
                                   Firefox                                                              Firefox                         
                                   to play                                                              to play                         
                                   audio,                                                               audio,                          
                                   the                                                                  the                             
                                   server                                                               server                          
                                   must                                                                 must                            
                                   serve the                                                            serve the                       
                                   file                                                                 file                            
                                   using the                                                            using the                       
                                   correct                                                              correct                         
                                   MIME                                                                 MIME                            
                                   type.                                                                type.                           

  `autoplay`   3            12     3.5       9          10.5         3.1      3            18           4         11           3        1.0

  `controls`   3            12     3.5       9          10.5         3.1      3            18           4         11           3        1.0

  `loop`       3            12     11        9          10.5         3.1      3            18           14        11           3        1.0

  `muted`      15           ≤18    11        No         15           6        4.4          18           14        14           6        1.0

  `preload`    3            12     43.5--4   9          15           3.1      3            18           4         14           3        1.0
                                                                                                                                        
               Defaults to                              Defaults to           Defaults to  Defaults to            Defaults to           Defaults to
               `metadata`                               `metadata`            `metadata`   `metadata`             `metadata`            `metadata`
               in Chrome                                in Opera 51.          in Chrome    in Chrome              in Opera 51.          in Samsung
               64.                                                            64.          64.                                          Internet
                                                        10.5--15                                                  11--14                9.0.

  `src`        3            12     3.5       9          10.5         3.1      3            18           4         11           3        1.0
  --------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [Web media
    technologies](https://developer.mozilla.org/en-US/docs/Web/Media)
    -   [Media container formats (file
        types)](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Containers)
    -   [Guide to audio codecs used on the
        web](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Audio_codecs)
-   [Web Audio
    API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API)
-   [`HTMLAudioElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLAudioElement)
-   [`<source>`](source)
-   [`<video>`](video)
-   [Learning area: Video and audio
    content](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content)
-   [Cross-browser audio
    basics](https://developer.mozilla.org/en-US/docs/Web/Guide/Audio_and_video_delivery/Cross-browser_audio_basics)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio){._attribution-link}
:::
