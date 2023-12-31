

# \<video\>: The Video Embed element



::: section-content
The `<video>` [HTML](../index) element embeds a media player which
supports video playback into the document. You can use `<video>` for
audio content as well, but the [`<audio>`](audio) element may provide a
more appropriate user experience.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<video\> {#html-demo-video .output-heading}

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
    <video controls width="250">
      <source src="/media/cc0-videos/flower.webm" type="video/webm" />

      <source src="/media/cc0-videos/flower.mp4" type="video/mp4" />

      Download the
      <a href="/media/cc0-videos/flower.webm">WEBM</a>
      or
      <a href="/media/cc0-videos/flower.mp4">MP4</a>
      video.
    </video>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
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

The above example shows simple usage of the `<video>` element. In a
similar manner to the [`<img>`](img) element, we include a path to the
media we want to display inside the `src` attribute; we can include
other attributes to specify information such as video width and height,
whether we want it to autoplay and loop, whether we want to show the
browser\'s default video controls, etc.

The content inside the opening and closing `<video></video>` tags is
shown as a fallback in browsers that don\'t support the element.
:::

## Attributes

::: section-content
Like all other HTML elements, this element supports the [global
attributes](../global_attributes).

[`autoplay`](#autoplay)

:   A Boolean attribute; if specified, the video automatically begins to
    play back as soon as it can do so without stopping to finish loading
    the data.

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

    To disable video autoplay, `autoplay="false"` will not work; the
    video will autoplay if the attribute is there in the `<video>` tag
    at all. To remove autoplay, the attribute needs to be removed
    altogether.

    In some browsers (e.g. Chrome 70.0) autoplay doesn\'t work if no
    `muted` attribute is present.

[`controls`](#controls)

:   If this attribute is present, the browser will offer controls to
    allow the user to control video playback, including volume, seeking,
    and pause/resume playback.

[`controlslist`](#controlslist) [Experimental]{.visually-hidden} [Non-standard]{.visually-hidden}

:   The
    [`controlslist`](https://wicg.github.io/controls-list/explainer.html){target="_blank"}
    attribute, when specified, helps the browser select what controls to
    show for the `video` element whenever the browser shows its own set
    of controls (that is, when the `controls` attribute is specified).

    The allowed values are `nodownload`, `nofullscreen` and
    `noremoteplayback`.

    Use the [`disablepictureinpicture`](#disablepictureinpicture)
    attribute if you want to disable the Picture-In-Picture mode (and
    the control).

[`crossorigin`](#crossorigin)

:   This
    [enumerated](https://developer.mozilla.org/en-US/docs/Glossary/Enumerated)
    attribute indicates whether to use CORS to fetch the related video.
    [CORS-enabled resources](../cors_enabled_image) can be reused in the
    [`<canvas>`](canvas) element without being *tainted*. The allowed
    values are:

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
    handled as if the enumerated keyword `anonymous` was used. See [CORS
    settings attributes](../attributes/crossorigin) for additional
    information.

[`disablepictureinpicture`](#disablepictureinpicture) [Experimental]{.visually-hidden}

:   Prevents the browser from suggesting a Picture-in-Picture context
    menu or to request Picture-in-Picture automatically in some cases.

[`disableremoteplayback`](#disableremoteplayback) [Experimental]{.visually-hidden}

:   A Boolean attribute used to disable the capability of remote
    playback in devices that are attached using wired (HDMI, DVI, etc.)
    and wireless technologies (Miracast, Chromecast, DLNA, AirPlay,
    etc.).

    In Safari, you can use
    [`x-webkit-airplay="deny"`](https://developer.apple.com/library/archive/documentation/AudioVideo/Conceptual/AirPlayGuide/OptingInorOutofAirPlay/OptingInorOutofAirPlay.html){target="_blank"}
    as a fallback.

[`height`](#height)

:   The height of the video\'s display area, in [CSS
    pixels](https://drafts.csswg.org/css-values/#px){target="_blank"}
    (absolute values only; [no
    percentages](https://html.spec.whatwg.org/multipage/embedded-content.html#dimension-attributes){target="_blank"}).

[`loop`](#loop)

:   A Boolean attribute; if specified, the browser will automatically
    seek back to the start upon reaching the end of the video.

[`muted`](#muted)

:   A Boolean attribute that indicates the default setting of the audio
    contained in the video. If set, the audio will be initially
    silenced. Its default value is `false`, meaning that the audio will
    be played when the video is played.

[`playsinline`](#playsinline)

:   A Boolean attribute indicating that the video is to be played
    \"inline\", that is within the element\'s playback area. Note that
    the absence of this attribute *does not* imply that the video will
    always be played in fullscreen.

[`poster`](#poster)

:   A URL for an image to be shown while the video is downloading. If
    this attribute isn\'t specified, nothing is displayed until the
    first frame is available, then the first frame is shown as the
    poster frame.

[`preload`](#preload)

:   This enumerated attribute is intended to provide a hint to the
    browser about what the author thinks will lead to the best user
    experience regarding what content is loaded before the video is
    played. It may have one of the following values:

    -   `none`: Indicates that the video should not be preloaded.
    -   `metadata`: Indicates that only video metadata (e.g. length) is
        fetched.
    -   `auto`: Indicates that the whole video file can be downloaded,
        even if the user is not expected to use it.
    -   *empty string*: Synonym of the `auto` value.

    The default value is different for each browser. The spec advises it
    to be set to `metadata`.

    ::: {#sect2 .notecard .note}
    **Note:**

    -   The `autoplay` attribute has precedence over `preload`. If
        `autoplay` is specified, the browser would obviously need to
        start downloading the video for playback.
    -   The specification does not force the browser to follow the value
        of this attribute; it is a mere hint.
    :::

[`src`](#src)

:   The URL of the video to embed. This is optional; you may instead use
    the [`<source>`](source) element within the video block to specify
    the video to embed.

[`width`](#width)

:   The width of the video\'s display area, in [CSS
    pixels](https://drafts.csswg.org/css-values/#px){target="_blank"}
    (absolute values only; [no
    percentages](https://html.spec.whatwg.org/multipage/embedded-content.html#dimension-attributes){target="_blank"}).
:::

## Events

::: section-content
<figure class="table-container">
<div class="_table">
<table class="no-markdown">
<thead>
<tr class="header">
<th scope="col">Event Name</th>
<th scope="col">Fired When</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/ScriptProcessorNode/audioprocess_event"><code>audioprocess</code></a>
<span class="visually-hidden">Deprecated</span></td>
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
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/load"
rel="internal"><code>load()</code></a> method is called to reload
it.</td>
</tr>
<tr class="odd">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/ended_event"><code>ended</code></a></td>
<td>Playback has stopped because the end of the media was reached.</td>
</tr>
<tr class="even">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/error_event"><code>error</code></a></td>
<td>An error occurred while fetching the media data, or the type of the
resource is not a supported media format.</td>
</tr>
<tr class="odd">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/loadeddata_event"><code>loadeddata</code></a></td>
<td>The first frame of the media has finished loading.</td>
</tr>
<tr class="even">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/loadedmetadata_event"><code>loadedmetadata</code></a></td>
<td>The metadata has been loaded.</td>
</tr>
<tr class="odd">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/loadstart_event"><code>loadstart</code></a></td>
<td>Fired when the browser has started to load the resource.</td>
</tr>
<tr class="even">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/pause_event"><code>pause</code></a></td>
<td>Playback has been paused.</td>
</tr>
<tr class="odd">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/play_event"><code>play</code></a></td>
<td>Playback has begun.</td>
</tr>
<tr class="even">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/playing_event"><code>playing </code></a></td>
<td>Playback is ready to start after having been paused or delayed due
to lack of data.</td>
</tr>
<tr class="odd">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/progress_event"><code>progress</code></a></td>
<td>Fired periodically as the browser loads a resource.</td>
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
<td>Playback has stopped because of a temporary lack of data.</td>
</tr>
</tbody>
</table>

</figure>
:::

## Usage notes {#usage_notes}

::: section-content
Browsers don\'t all support the same video formats; you can provide
multiple sources inside nested [`<source>`](source) elements, and the
browser will then use the first one it understands.

::: code-example
[html]{.language-name}

``` {signature="mCju5VvpFFVY1pIvMFUv4y82OMWccxnVrQNPUHbLNAI=" data-language="html"}
<video controls>
  <source src="myVideo.webm" type="video/webm" />
  <source src="myVideo.mp4" type="video/mp4" />
  <p>
    Your browser doesn't support HTML video. Here is a
    <a href="myVideo.mp4">link to the video</a> instead.
  </p>
</video>
```
:::

We offer a substantive and thorough [guide to media file
types](https://developer.mozilla.org/en-US/docs/Web/Media/Formats) and
the [guide to the codecs supported for
video](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs).
Also available is a guide to [audio codecs that can be used with
them](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Audio_codecs).

Other usage notes:

-   If you don\'t specify the `controls` attribute, the video won\'t
    include the browser\'s default controls; you can create your own
    custom controls using JavaScript and the
    [`HTMLMediaElement`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement)
    API. See [Creating a cross-browser video
    player](https://developer.mozilla.org/en-US/docs/Web/Guide/Audio_and_video_delivery/cross_browser_video_player)
    for more details.
-   To allow precise control over your video (and audio) content,
    `HTMLMediaElement`s fire many different
    [events](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement#events).
    In addition to providing controllability, these events let you
    monitor the progress of both download and playback of the media, as
    well as the playback state and position.
-   You can use the
    [`object-position`](https://developer.mozilla.org/en-US/docs/Web/CSS/object-position)
    property to adjust the positioning of the video within the
    element\'s frame, and the
    [`object-fit`](https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit)
    property to control how the video\'s size is adjusted to fit within
    the frame.
-   To show subtitles/captions along with your video, you can use some
    JavaScript along with the [`<track>`](track) element and the
    [WebVTT](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)
    format. See [Adding captions and subtitles to HTML
    video](https://developer.mozilla.org/en-US/docs/Web/Guide/Audio_and_video_delivery/Adding_captions_and_subtitles_to_HTML5_video)
    for more information.
-   You can play audio files using a `<video>` element. This can be
    useful if, for example, you need to perform audio with a
    [WebVTT](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API)
    transcript, since the [`<audio>`](audio) element doesn\'t allow
    captions using WebVTT.
-   To test the fallback content on browsers that support the element,
    you can replace `<video>` with a non-existing element like
    `<notavideo>`.

A good general source of information on using HTML `<video>` is the
[Video and audio
content](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content)
beginner\'s tutorial.
:::

### Styling with CSS {#styling_with_css}

::: section-content
The `<video>` element is a replaced element --- its
[`display`](https://developer.mozilla.org/en-US/docs/Web/CSS/display)
value is `inline` by default, but its default width and height in the
viewport is defined by the video being embedded.

There are no special considerations for styling `<video>`; a common
strategy is to give it a `display` value of `block` to make it easier to
position, size, etc., and then provide styling and layout information as
required. [Video player styling
basics](https://developer.mozilla.org/en-US/docs/Web/Guide/Audio_and_video_delivery/Video_player_styling_basics)
provides some useful styling techniques.
:::

### Detecting track addition and removal {#detecting_track_addition_and_removal}

::: section-content
You can detect when tracks are added to and removed from a `<video>`
element using the
[`addtrack`](https://developer.mozilla.org/en-US/docs/Web/API/VideoTrackList/addtrack_event)
and
[`removetrack`](https://developer.mozilla.org/en-US/docs/Web/API/VideoTrackList/removetrack_event)
events. However, these events aren\'t sent directly to the `<video>`
element itself. Instead, they\'re sent to the track list object within
the `<video>` element\'s
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

For example, to detect when audio tracks are added to or removed from a
`<video>` element, you can use code like this:

::: code-example
[js]{.language-name}

``` {signature="P1adpaWeLeJpUywZ67D+U+xhFJnNqeKt09kAHkaso4c=" data-language="js"}
const elem = document.querySelector("video");

elem.audioTracks.onaddtrack = (event) => {
  trackEditor.addTrack(event.track);
};

elem.audioTracks.onremovetrack = (event) => {
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
[`addtrack`](https://developer.mozilla.org/en-US/docs/Web/API/VideoTrackList/addtrack_event)
and
[`removetrack`](https://developer.mozilla.org/en-US/docs/Web/API/VideoTrackList/removetrack_event)
events.
:::

### Server support for video {#server_support_for_video}

::: section-content
If the MIME type for the video is not set correctly on the server, the
video may not show or show a gray box containing an X (if JavaScript is
enabled).

If you use Apache Web Server to serve Ogg Theora videos, you can fix
this problem by adding the video file type extensions to \"video/ogg\"
MIME type. The most common video file type extensions are \".ogm\",
\".ogv\", or \".ogg\". To do this, edit the \"mime.types\" file in
\"/etc/apache\" or use the `"AddType"` configuration directive in
`httpd.conf`.

``` {data-language="plain"}
AddType video/ogg .ogm
AddType video/ogg .ogv
AddType video/ogg .ogg
```

If you serve your videos as WebM, you can fix this problem for the
Apache Web Server by adding the extension used by your video files
(\".webm\" is the most common one) to the MIME type \"video/webm\" via
the \"mime.types\" file in \"/etc/apache\" or via the \"AddType\"
configuration directive in `httpd.conf`.

``` {data-language="plain"}
AddType video/webm .webm
```

Your web host may provide an easy interface to MIME type configuration
changes for new technologies until a global update naturally occurs.
:::

## Examples

### Single source {#single_source}

::: section-content
This example plays a video when activated, providing the user with the
browser\'s default video controls to control playback.

#### HTML

::: code-example
[html]{.language-name}

``` {signature="w9j9w9v6znMZNPHCXUvp5XjIjZ6oNzBi9clDzDwBT+Y=" data-language="html"}
<!-- Simple video example -->
<!-- 'Big Buck Bunny' licensed under CC 3.0 by the Blender foundation. Hosted by archive.org -->
<!-- Poster from peach.blender.org -->
<video
  controls
  src="https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.mp4"
  poster="https://peach.blender.org/wp-content/uploads/title_anouncement.jpg?x11217"
  width="620">
  Sorry, your browser doesn't support embedded videos, but don't worry, you can
  <a href="https://archive.org/details/BigBuckBunny_124">download it</a>
  and watch it with your favorite video player!
</video>
```
:::

#### Result

::: {#sect3 .code-example}
::: iframe
:::
:::

Until the video starts playing, the image provided in the `poster`
attribute is displayed in its place. If the browser doesn\'t support
video playback, the fallback text is displayed.
:::

### Multiple sources {#multiple_sources}

::: section-content
This example builds on the last one, offering three different sources
for the media; this allows the video to be watched regardless of which
video codecs are supported by the browser.

#### HTML {#html_2}

::: code-example
[html]{.language-name}

``` {signature="63xmYMO3MubFVlij4Mr8w2cuUqJ9+T/U3hQD/e0QHTw=" data-language="html"}
<!-- Using multiple sources as fallbacks for a video tag -->
<!-- 'Elephants Dream' by Orange Open Movie Project Studio, licensed under CC-3.0, hosted by archive.org -->
<!-- Poster hosted by Wikimedia -->
<video
  width="620"
  controls
  poster="https://upload.wikimedia.org/wikipedia/commons/e/e8/Elephants_Dream_s5_both.jpg">
  <source
    src="https://archive.org/download/ElephantsDream/ed_hd.ogv"
    type="video/ogg" />
  <source
    src="https://archive.org/download/ElephantsDream/ed_hd.avi"
    type="video/avi" />
  <source
    src="https://archive.org/download/ElephantsDream/ed_1024_512kb.mp4"
    type="video/mp4" />

  Sorry, your browser doesn't support embedded videos, but don't worry, you can
  <a href="https://archive.org/download/ElephantsDream/ed_1024_512kb.mp4">
    download the MP4
  </a>
  and watch it with your favorite video player!
</video>
```
:::

#### Result {#result_2}

::: {#sect4 .code-example}
::: iframe
:::
:::

First
[Ogg](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Containers#ogg)
is tried. If that can\'t be played, then AVI is tried. Finally,
[MP4](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Containers#mpeg-4_mp4)
is tried. A fallback message is displayed if the video element isn\'t
supported, but not if all sources fail.

Some media file types let you provide more specific information using
the
[`codecs`](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/codecs_parameter)
parameter as part of the file\'s type string. A relatively simple
example is `video/webm; codecs="vp8, vorbis"`, which says that the file
is a
[WebM](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Containers#webm)
video using
[VP8](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp8)
for its video and
[Vorbis](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Audio_codecs#vorbis)
for audio.
:::

## Accessibility concerns {#accessibility_concerns}

::: section-content
Videos should provide both captions and transcripts that accurately
describe its content (see [Adding captions and subtitles to HTML
video](https://developer.mozilla.org/en-US/docs/Web/Guide/Audio_and_video_delivery/Adding_captions_and_subtitles_to_HTML5_video)
for more information on how to implement these). Captions allow people
who are experiencing hearing loss to understand a video\'s audio content
as the video is being played, while transcripts allow people who need
additional time to be able to review audio content at a pace and format
that is comfortable for them.

It\'s worth noting that while you can caption audio-only media, you can
only do so when playing audio in a
[`<video>`](video){aria-current="page"} element, since the video region
of the element is used to present the captions. This is one of the
special scenarios in which it\'s useful to play audio in a video
element.

If automatic captioning services are used, it is important to review the
generated content to ensure it accurately represents the source video.

In addition to spoken dialog, subtitles and transcripts should also
identify music and sound effects that communicate important information.
This includes emotion and tone:

``` {data-language="plain"}
14
00:03:14 --> 00:03:18
[Dramatic rock music]

15
00:03:19 --> 00:03:21
[whispering] What's that off in the distance?

16
00:03:22 --> 00:03:24
It's… it's a…

16 00:03:25 --> 00:03:32
[Loud thumping]
[Dishes clattering]
```

Captions should not obstruct the main subject of the video. They can be
positioned using [the `align` VTT cue
setting](https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API#cue_settings).

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
phrasing content, embedded content. If it has a <a href="video#controls"
aria-current="page"><code>controls</code></a> attribute: interactive
content and palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><p>If the element has a <a href="video#src"
aria-current="page"><code>src</code></a> attribute: zero or more <a
href="track"><code>&lt;track&gt;</code></a> elements, followed by
transparent content that contains no media elements–that is no <a
href="audio"><code>&lt;audio&gt;</code></a> or <a href="video"
aria-current="page"><code>&lt;video&gt;</code></a>.</p>
<p>Else: zero or more <a href="source"><code>&lt;source&gt;</code></a>
elements, followed by zero or more <a
href="track"><code>&lt;track&gt;</code></a> elements, followed by
transparent content that contains no media elements–that is no <a
href="audio"><code>&lt;audio&gt;</code></a> or <a href="video"
aria-current="page"><code>&lt;video&gt;</code></a>.</p></td>
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
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLVideoElement"><code>HTMLVideoElement</code></a></td>
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
  the-video-element]{.small}](https://html.spec.whatwg.org/multipage/media.html#the-video-element)

  --------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                                            Desktop                                                                                     Mobile                                                                                                                                                                                                  
  ----------------------------------------- ------------ ------ -------------------------------------- ---------- ------------ -------- ------------ ------------ -------------------------------------- ------------ ------------------------------------------------------------------------------------------------------------------------- ------------
                                            Chrome       Edge   Firefox                                Internet   Opera        Safari   WebView      Chrome       Firefox for Android                    Opera        Safari on IOS                                                                                                             Samsung
                                                                                                       Explorer                         Android      Android                                             Android                                                                                                                                Internet

  `video`                                   3            12     3.5                                    9          10.5         3.1      4.4          18           4                                      14           3                                                                                                                         1.0

  `aspect_ratio_computed_from_attributes`   79           79     71                                     No         66           14       79           79           79                                     57           14                                                                                                                        12.0

  `autoplay`                                3            12     3.5                                    9          10.5         3.1      4.4          18           4                                      14           10                                                                                                                        1.0
                                                                                                                                                                                                                                                                                                                                                
                                                                                                                                                                                                                      Only available for videos that have [no sound or have the audio track                                                     
                                                                                                                                                                                                                      disabled](https://developer.apple.com/library/content/releasenotes/General/WhatsNewInSafari/Articles/Safari_10_0.html).   

  `controls`                                3            12     3.5                                    9          10.5         3.1      4.4          18           4                                      14           3                                                                                                                         1.0

  `crossorigin`                             33           ≤18    74                                     No         20           10       4.4.3        33           79                                     20           10                                                                                                                        2.0
                                                                                                                                                                                                                                                                                                                                                
                                                                12--74                                                                                            14--79                                                                                                                                                                        
                                                                                                                                                                                                                                                                                                                                                
                                                                With `crossorigin="use-credentials"`,                                                             With `crossorigin="use-credentials"`,                                                                                                                                         
                                                                cookies aren\'t sent during seek. See                                                             cookies aren\'t sent during seek. See                                                                                                                                         
                                                                [bug                                                                                              [bug                                                                                                                                                                          
                                                                1532722](https://bugzil.la/1532722).                                                              1532722](https://bugzil.la/1532722).                                                                                                                                          

  `height`                                  3            12     3.5                                    9          10.5         3.1      4.4          18           4                                      14           3                                                                                                                         1.0

  `loop`                                    3            12     11                                     9          10.5         3.1      4.4          18           14                                     14           6                                                                                                                         1.0

  `muted`                                   30           12     11                                     10         Yes          5        4.4          30           14                                     18           No                                                                                                                        2.0

  `poster`                                  3            12     3.6                                    9          10.5         3.1      4.4          18           4                                      14           3                                                                                                                         1.0

  `preload`                                 3            12     4                                      9          Yes          3.1      Yes          Yes          4                                      Yes          3                                                                                                                         Yes
                                                                                                                                                                                                                                                                                                                                                
                                            Defaults to                                                           Defaults to           Defaults to  Defaults to                                         Defaults to                                                                                                                            Defaults to
                                            `metadata`                                                            `metadata`            `metadata`   `metadata`                                          `metadata`                                                                                                                             `metadata`
                                            in Chrome                                                             in Opera 51.          in Chrome    in Chrome                                           in Opera 51.                                                                                                                           in Samsung
                                            64.                                                                                         64.          64.                                                                                                                                                                                        Internet
                                                                                                                                                                                                                                                                                                                                                9.0.

  `src`                                     3            12     3.5                                    9          10.5         3.1      4.4          18           4                                      14           3                                                                                                                         1.0

  `width`                                   3            12     3.5                                    9          10.5         3.1      4.4          18           4                                      14           3                                                                                                                         1.0
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [Guide to media types and formats on the
    web](https://developer.mozilla.org/en-US/docs/Web/Media/Formats)
    -   [Media container formats (file
        types)](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Containers)
    -   [Web video codec
        guide](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs)
    -   [Web audio codec
        guide](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Audio_codecs)
-   Positioning and sizing the picture within its frame:
    [`object-position`](https://developer.mozilla.org/en-US/docs/Web/CSS/object-position)
    and
    [`object-fit`](https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit)
-   [`<audio>`](audio)
-   [Using HTML audio and
    video](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content)
-   [Manipulating video using
    canvas](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Manipulating_video_using_canvas)
-   [Configuring servers for Ogg
    media](https://developer.mozilla.org/en-US/docs/Web/HTTP/Configuring_servers_for_Ogg_media)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video){._attribution-link}
:::
