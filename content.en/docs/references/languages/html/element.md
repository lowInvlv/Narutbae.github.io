

# HTML elements reference



::: section-content
This page lists all the
[HTML](https://developer.mozilla.org/en-US/docs/Glossary/HTML)
[elements](https://developer.mozilla.org/en-US/docs/Glossary/Element),
which are created using
[tags](https://developer.mozilla.org/en-US/docs/Glossary/Tag).

They are grouped by function to help you find what you have in mind
easily. An alphabetical list of all elements is provided in the sidebar
on every element\'s page as well as this one.

::: {#sect1 .notecard .note}
**Note:** For more information about the basics of HTML elements and
attributes, see [the section on elements in the Introduction to HTML
article](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML#elements_%e2%80%94_the_basic_building_blocks).
:::
:::

## Main root {#main_root}

::: section-content
<figure class="table-container">
<div class="_table">
<table>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element/html"><code>&lt;html&gt;</code></a></td>
<td>Represents the root (top-level element) of an HTML document, so it
is also referred to as the <em>root element</em>. All other elements
must be descendants of this element.</td>
</tr>
</tbody>
</table>

</figure>
:::

## Document metadata {#document_metadata}

::: section-content
Metadata contains information about the page. This includes information
about styles, scripts and data to help software ([search
engines](https://developer.mozilla.org/en-US/docs/Glossary/Search_engine),
[browsers](https://developer.mozilla.org/en-US/docs/Glossary/Browser),
etc.) use and render the page. Metadata for styles and scripts may be
defined in the page or linked to another file that has the information.

<figure class="table-container">
<div class="_table">
<table>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element/base"><code>&lt;base&gt;</code></a></td>
<td>Specifies the base URL to use for all relative URLs in a document.
There can be only one such element in a document.</td>
</tr>
<tr class="even">
<td><a href="element/head"><code>&lt;head&gt;</code></a></td>
<td>Contains machine-readable information (metadata) about the document,
like its <a href="element/title">title</a>, <a
href="element/script">scripts</a>, and <a href="element/style">style
sheets</a>.</td>
</tr>
<tr class="odd">
<td><a href="element/link"><code>&lt;link&gt;</code></a></td>
<td>Specifies relationships between the current document and an external
resource. This element is most commonly used to link to CSS but is also
used to establish site icons (both "favicon" style icons and icons for
the home screen and apps on mobile devices) among other things.</td>
</tr>
<tr class="even">
<td><a href="element/meta"><code>&lt;meta&gt;</code></a></td>
<td>Represents <a
href="https://developer.mozilla.org/en-US/docs/Glossary/Metadata">metadata</a>
that cannot be represented by other HTML meta-related elements, like <a
href="element/base"><code>&lt;base&gt;</code></a>, <a
href="element/link"><code>&lt;link&gt;</code></a>, <a
href="element/script"><code>&lt;script&gt;</code></a>, <a
href="element/style"><code>&lt;style&gt;</code></a> and <a
href="element/title"><code>&lt;title&gt;</code></a>.</td>
</tr>
<tr class="odd">
<td><a href="element/style"><code>&lt;style&gt;</code></a></td>
<td>Contains style information for a document or part of a document. It
contains CSS, which is applied to the contents of the document
containing this element.</td>
</tr>
<tr class="even">
<td><a href="element/title"><code>&lt;title&gt;</code></a></td>
<td>Defines the document's title that is shown in a <a
href="https://developer.mozilla.org/en-US/docs/Glossary/Browser">browser</a>'s
title bar or a page's tab. It only contains text; tags within the
element are ignored.</td>
</tr>
</tbody>
</table>

</figure>
:::

## Sectioning root {#sectioning_root}

::: section-content
<figure class="table-container">
<div class="_table">
<table>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element/body"><code>&lt;body&gt;</code></a></td>
<td>represents the content of an HTML document. There can be only one
such element in a document.</td>
</tr>
</tbody>
</table>

</figure>
:::

## Content sectioning {#content_sectioning}

::: section-content
Content sectioning elements allow you to organize the document content
into logical pieces. Use the sectioning elements to create a broad
outline for your page content, including header and footer navigation,
and heading elements to identify sections of content.

<figure class="table-container">
<div class="_table">
<table>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element/address"><code>&lt;address&gt;</code></a></td>
<td>Indicates that the enclosed HTML provides contact information for a
person or people, or for an organization.</td>
</tr>
<tr class="even">
<td><a href="element/article"><code>&lt;article&gt;</code></a></td>
<td>Represents a self-contained composition in a document, page,
application, or site, which is intended to be independently
distributable or reusable (e.g., in syndication). Examples include a
forum post, a magazine or newspaper article, a blog entry, a product
card, a user-submitted comment, an interactive widget or gadget, or any
other independent item of content.</td>
</tr>
<tr class="odd">
<td><a href="element/aside"><code>&lt;aside&gt;</code></a></td>
<td>Represents a portion of a document whose content is only indirectly
related to the document's main content. Asides are frequently presented
as sidebars or call-out boxes.</td>
</tr>
<tr class="even">
<td><a href="element/footer"><code>&lt;footer&gt;</code></a></td>
<td>Represents a footer for its nearest ancestor <a
href="content_categories#sectioning_content">sectioning content</a> or
<a href="element/heading_elements">sectioning root</a> element. A
<code>&lt;footer&gt;</code> typically contains information about the
author of the section, copyright data, or links to related
documents.</td>
</tr>
<tr class="odd">
<td><a href="element/header"><code>&lt;header&gt;</code></a></td>
<td>Represents introductory content, typically a group of introductory
or navigational aids. It may contain some heading elements but also a
logo, a search form, an author name, and other elements.</td>
</tr>
<tr class="even">
<td><a href="element/heading_elements"><code>&lt;h1&gt;</code></a>, <a
href="element/heading_elements"><code>&lt;h2&gt;</code></a>, <a
href="element/heading_elements"><code>&lt;h3&gt;</code></a>, <a
href="element/heading_elements"><code>&lt;h4&gt;</code></a>, <a
href="element/heading_elements"><code>&lt;h5&gt;</code></a>, <a
href="element/heading_elements"><code>&lt;h6&gt;</code></a></td>
<td>Represent six levels of section headings. <code>&lt;h1&gt;</code> is
the highest section level and <code>&lt;h6&gt;</code> is the
lowest.</td>
</tr>
<tr class="odd">
<td><a href="element/hgroup"><code>&lt;hgroup&gt;</code></a></td>
<td>Represents a heading grouped with any secondary content, such as
subheadings, an alternative title, or a tagline.</td>
</tr>
<tr class="even">
<td><a href="element/main"><code>&lt;main&gt;</code></a></td>
<td>Represents the dominant content of the body of a document. The main
content area consists of content that is directly related to or expands
upon the central topic of a document, or the central functionality of an
application.</td>
</tr>
<tr class="odd">
<td><a href="element/nav"><code>&lt;nav&gt;</code></a></td>
<td>Represents a section of a page whose purpose is to provide
navigation links, either within the current document or to other
documents. Common examples of navigation sections are menus, tables of
contents, and indexes.</td>
</tr>
<tr class="even">
<td><a href="element/section"><code>&lt;section&gt;</code></a></td>
<td>Represents a generic standalone section of a document, which doesn't
have a more specific semantic element to represent it. Sections should
always have a heading, with very few exceptions.</td>
</tr>
<tr class="odd">
<td><a href="element/search"><code>&lt;search&gt;</code></a></td>
<td>Represents a part that contains a set of form controls or other
content related to performing a search or filtering operation.</td>
</tr>
</tbody>
</table>

</figure>
:::

## Text content {#text_content}

::: section-content
Use HTML text content elements to organize blocks or sections of content
placed between the opening [`<body>`](element/body) and closing
`</body>` tags. Important for
[accessibility](https://developer.mozilla.org/en-US/docs/Glossary/Accessibility)
and [SEO](https://developer.mozilla.org/en-US/docs/Glossary/SEO), these
elements identify the purpose or structure of that content.

<figure class="table-container">
<div class="_table">
<table>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a
href="element/blockquote"><code>&lt;blockquote&gt;</code></a></td>
<td>Indicates that the enclosed text is an extended quotation. Usually,
this is rendered visually by indentation. A URL for the source of the
quotation may be given using the <code>cite</code> attribute, while a
text representation of the source can be given using the <a
href="element/cite"><code>&lt;cite&gt;</code></a> element.</td>
</tr>
<tr class="even">
<td><a href="element/dd"><code>&lt;dd&gt;</code></a></td>
<td>Provides the description, definition, or value for the preceding
term (<a href="element/dt"><code>&lt;dt&gt;</code></a>) in a description
list (<a href="element/dl"><code>&lt;dl&gt;</code></a>).</td>
</tr>
<tr class="odd">
<td><a href="element/div"><code>&lt;div&gt;</code></a></td>
<td>The generic container for flow content. It has no effect on the
content or layout until styled in some way using CSS (e.g., styling is
directly applied to it, or some kind of layout model like <a
href="https://developer.mozilla.org/en-US/docs/Glossary/Flexbox">flexbox</a>
is applied to its parent element).</td>
</tr>
<tr class="even">
<td><a href="element/dl"><code>&lt;dl&gt;</code></a></td>
<td>Represents a description list. The element encloses a list of groups
of terms (specified using the <a
href="element/dt"><code>&lt;dt&gt;</code></a> element) and descriptions
(provided by <a href="element/dd"><code>&lt;dd&gt;</code></a> elements).
Common uses for this element are to implement a glossary or to display
metadata (a list of key-value pairs).</td>
</tr>
<tr class="odd">
<td><a href="element/dt"><code>&lt;dt&gt;</code></a></td>
<td>Specifies a term in a description or definition list, and as such
must be used inside a <a href="element/dl"><code>&lt;dl&gt;</code></a>
element. It is usually followed by a <a
href="element/dd"><code>&lt;dd&gt;</code></a> element; however, multiple
<code>&lt;dt&gt;</code> elements in a row indicate several terms that
are all defined by the immediate next <a
href="element/dd"><code>&lt;dd&gt;</code></a> element.</td>
</tr>
<tr class="even">
<td><a
href="element/figcaption"><code>&lt;figcaption&gt;</code></a></td>
<td>Represents a caption or legend describing the rest of the contents
of its parent <a href="element/figure"><code>&lt;figure&gt;</code></a>
element.</td>
</tr>
<tr class="odd">
<td><a href="element/figure"><code>&lt;figure&gt;</code></a></td>
<td>Represents self-contained content, potentially with an optional
caption, which is specified using the <a
href="element/figcaption"><code>&lt;figcaption&gt;</code></a> element.
The figure, its caption, and its contents are referenced as a single
unit.</td>
</tr>
<tr class="even">
<td><a href="element/hr"><code>&lt;hr&gt;</code></a></td>
<td>Represents a thematic break between paragraph-level elements: for
example, a change of scene in a story, or a shift of topic within a
section.</td>
</tr>
<tr class="odd">
<td><a href="element/li"><code>&lt;li&gt;</code></a></td>
<td>Represents an item in a list. It must be contained in a parent
element: an ordered list (<a
href="element/ol"><code>&lt;ol&gt;</code></a>), an unordered list (<a
href="element/ul"><code>&lt;ul&gt;</code></a>), or a menu (<a
href="element/menu"><code>&lt;menu&gt;</code></a>). In menus and
unordered lists, list items are usually displayed using bullet points.
In ordered lists, they are usually displayed with an ascending counter
on the left, such as a number or letter.</td>
</tr>
<tr class="even">
<td><a href="element/menu"><code>&lt;menu&gt;</code></a></td>
<td>A semantic alternative to <a
href="element/ul"><code>&lt;ul&gt;</code></a>, but treated by browsers
(and exposed through the accessibility tree) as no different than <a
href="element/ul"><code>&lt;ul&gt;</code></a>. It represents an
unordered list of items (which are represented by <a
href="element/li"><code>&lt;li&gt;</code></a> elements).</td>
</tr>
<tr class="odd">
<td><a href="element/ol"><code>&lt;ol&gt;</code></a></td>
<td>Represents an ordered list of items — typically rendered as a
numbered list.</td>
</tr>
<tr class="even">
<td><a href="element/p"><code>&lt;p&gt;</code></a></td>
<td>Represents a paragraph. Paragraphs are usually represented in visual
media as blocks of text separated from adjacent blocks by blank lines
and/or first-line indentation, but HTML paragraphs can be any structural
grouping of related content, such as images or form fields.</td>
</tr>
<tr class="odd">
<td><a href="element/pre"><code>&lt;pre&gt;</code></a></td>
<td>Represents preformatted text which is to be presented exactly as
written in the HTML file. The text is typically rendered using a
non-proportional, or <a
href="https://en.wikipedia.org/wiki/Monospaced_font"
target="_blank">monospaced</a>, font. Whitespace inside this element is
displayed as written.</td>
</tr>
<tr class="even">
<td><a href="element/ul"><code>&lt;ul&gt;</code></a></td>
<td>Represents an unordered list of items, typically rendered as a
bulleted list.</td>
</tr>
</tbody>
</table>

</figure>
:::

## Inline text semantics {#inline_text_semantics}

::: section-content
Use the HTML inline text semantic to define the meaning, structure, or
style of a word, line, or any arbitrary piece of text.

<figure class="table-container">
<div class="_table">
<table>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element/a"><code>&lt;a&gt;</code></a></td>
<td>Together with its <code>href</code> attribute, creates a hyperlink
to web pages, files, email addresses, locations within the current page,
or anything else a URL can address.</td>
</tr>
<tr class="even">
<td><a href="element/abbr"><code>&lt;abbr&gt;</code></a></td>
<td>Represents an abbreviation or acronym.</td>
</tr>
<tr class="odd">
<td><a href="element/b"><code>&lt;b&gt;</code></a></td>
<td>Used to draw the reader's attention to the element's contents, which
are not otherwise granted special importance. This was formerly known as
the Boldface element, and most browsers still draw the text in boldface.
However, you should not use <code>&lt;b&gt;</code> for styling text or
granting importance. If you wish to create boldface text, you should use
the CSS <a
href="https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight"><code>font-weight</code></a>
property. If you wish to indicate an element is of special importance,
you should use the strong element.</td>
</tr>
<tr class="even">
<td><a href="element/bdi"><code>&lt;bdi&gt;</code></a></td>
<td>Tells the browser's bidirectional algorithm to treat the text it
contains in isolation from its surrounding text. It's particularly
useful when a website dynamically inserts some text and doesn't know the
directionality of the text being inserted.</td>
</tr>
<tr class="odd">
<td><a href="element/bdo"><code>&lt;bdo&gt;</code></a></td>
<td>Overrides the current directionality of text, so that the text
within is rendered in a different direction.</td>
</tr>
<tr class="even">
<td><a href="element/br"><code>&lt;br&gt;</code></a></td>
<td>Produces a line break in text (carriage-return). It is useful for
writing a poem or an address, where the division of lines is
significant.</td>
</tr>
<tr class="odd">
<td><a href="element/cite"><code>&lt;cite&gt;</code></a></td>
<td>Used to mark up the title of a cited creative work. The reference
may be in an abbreviated form according to context-appropriate
conventions related to citation metadata.</td>
</tr>
<tr class="even">
<td><a href="element/code"><code>&lt;code&gt;</code></a></td>
<td>Displays its contents styled in a fashion intended to indicate that
the text is a short fragment of computer code. By default, the content
text is displayed using the user agent's default monospace font.</td>
</tr>
<tr class="odd">
<td><a href="element/data"><code>&lt;data&gt;</code></a></td>
<td>Links a given piece of content with a machine-readable translation.
If the content is time- or date-related, the<code>&lt;time&gt;</code>
element must be used.</td>
</tr>
<tr class="even">
<td><a href="element/dfn"><code>&lt;dfn&gt;</code></a></td>
<td>Used to indicate the term being defined within the context of a
definition phrase or sentence. The ancestor <a
href="element/p"><code>&lt;p&gt;</code></a> element, the <a
href="element/dt"><code>&lt;dt&gt;</code></a>/<a
href="element/dd"><code>&lt;dd&gt;</code></a> pairing, or the nearest
section ancestor of the <code>&lt;dfn&gt;</code> element, is considered
to be the definition of the term.</td>
</tr>
<tr class="odd">
<td><a href="element/em"><code>&lt;em&gt;</code></a></td>
<td>Marks text that has stress emphasis. The <code>&lt;em&gt;</code>
element can be nested, with each nesting level indicating a greater
degree of emphasis.</td>
</tr>
<tr class="even">
<td><a href="element/i"><code>&lt;i&gt;</code></a></td>
<td>Represents a range of text that is set off from the normal text for
some reason, such as idiomatic text, technical terms, and taxonomical
designations, among others. Historically, these have been presented
using italicized type, which is the original source of the
<code>&lt;i&gt;</code> naming of this element.</td>
</tr>
<tr class="odd">
<td><a href="element/kbd"><code>&lt;kbd&gt;</code></a></td>
<td>Represents a span of inline text denoting textual user input from a
keyboard, voice input, or any other text entry device. By convention,
the user agent defaults to rendering the contents of a
<code>&lt;kbd&gt;</code> element using its default monospace font,
although this is not mandated by the HTML standard.</td>
</tr>
<tr class="even">
<td><a href="element/mark"><code>&lt;mark&gt;</code></a></td>
<td>Represents text which is marked or highlighted for reference or
notation purposes due to the marked passage's relevance in the enclosing
context.</td>
</tr>
<tr class="odd">
<td><a href="element/q"><code>&lt;q&gt;</code></a></td>
<td>Indicates that the enclosed text is a short inline quotation. Most
modern browsers implement this by surrounding the text in quotation
marks. This element is intended for short quotations that don't require
paragraph breaks; for long quotations use the <a
href="element/blockquote"><code>&lt;blockquote&gt;</code></a>
element.</td>
</tr>
<tr class="even">
<td><a href="element/rp"><code>&lt;rp&gt;</code></a></td>
<td>Used to provide fall-back parentheses for browsers that do not
support the display of ruby annotations using the <a
href="element/ruby"><code>&lt;ruby&gt;</code></a> element. One
<code>&lt;rp&gt;</code> element should enclose each of the opening and
closing parentheses that wrap the <a
href="element/rt"><code>&lt;rt&gt;</code></a> element that contains the
annotation's text.</td>
</tr>
<tr class="odd">
<td><a href="element/rt"><code>&lt;rt&gt;</code></a></td>
<td>Specifies the ruby text component of a ruby annotation, which is
used to provide pronunciation, translation, or transliteration
information for East Asian typography. The <code>&lt;rt&gt;</code>
element must always be contained within a <a
href="element/ruby"><code>&lt;ruby&gt;</code></a> element.</td>
</tr>
<tr class="even">
<td><a href="element/ruby"><code>&lt;ruby&gt;</code></a></td>
<td>Represents small annotations that are rendered above, below, or next
to base text, usually used for showing the pronunciation of East Asian
characters. It can also be used for annotating other kinds of text, but
this usage is less common.</td>
</tr>
<tr class="odd">
<td><a href="element/s"><code>&lt;s&gt;</code></a></td>
<td>Renders text with a strikethrough, or a line through it. Use the
<code>&lt;s&gt;</code> element to represent things that are no longer
relevant or no longer accurate. However, <code>&lt;s&gt;</code> is not
appropriate when indicating document edits; for that, use the del and
ins elements, as appropriate.</td>
</tr>
<tr class="even">
<td><a href="element/samp"><code>&lt;samp&gt;</code></a></td>
<td>Used to enclose inline text which represents sample (or quoted)
output from a computer program. Its contents are typically rendered
using the browser's default monospaced font (such as <a
href="https://en.wikipedia.org/wiki/Courier_(typeface)"
target="_blank">Courier</a> or Lucida Console).</td>
</tr>
<tr class="odd">
<td><a href="element/small"><code>&lt;small&gt;</code></a></td>
<td>Represents side-comments and small print, like copyright and legal
text, independent of its styled presentation. By default, it renders
text within it one font size smaller, such as from <code>small</code> to
<code>x-small</code>.</td>
</tr>
<tr class="even">
<td><a href="element/span"><code>&lt;span&gt;</code></a></td>
<td>A generic inline container for phrasing content, which does not
inherently represent anything. It can be used to group elements for
styling purposes (using the <code>class</code> or <code>id</code>
attributes), or because they share attribute values, such as
<code>lang</code>. It should be used only when no other semantic element
is appropriate. <code>&lt;span&gt;</code> is very much like a div
element, but div is a <a
href="https://developer.mozilla.org/en-US/docs/Glossary/Block-level_content">block-level
element</a> whereas a <code>&lt;span&gt;</code> is an <a
href="https://developer.mozilla.org/en-US/docs/Glossary/Inline-level_content">inline-level
element</a>.</td>
</tr>
<tr class="odd">
<td><a href="element/strong"><code>&lt;strong&gt;</code></a></td>
<td>Indicates that its contents have strong importance, seriousness, or
urgency. Browsers typically render the contents in bold type.</td>
</tr>
<tr class="even">
<td><a href="element/sub"><code>&lt;sub&gt;</code></a></td>
<td>Specifies inline text which should be displayed as subscript for
solely typographical reasons. Subscripts are typically rendered with a
lowered baseline using smaller text.</td>
</tr>
<tr class="odd">
<td><a href="element/sup"><code>&lt;sup&gt;</code></a></td>
<td>Specifies inline text which is to be displayed as superscript for
solely typographical reasons. Superscripts are usually rendered with a
raised baseline using smaller text.</td>
</tr>
<tr class="even">
<td><a href="element/time"><code>&lt;time&gt;</code></a></td>
<td>Represents a specific period in time. It may include the
<code>datetime</code> attribute to translate dates into machine-readable
format, allowing for better search engine results or custom features
such as reminders.</td>
</tr>
<tr class="odd">
<td><a href="element/u"><code>&lt;u&gt;</code></a></td>
<td>Represents a span of inline text which should be rendered in a way
that indicates that it has a non-textual annotation. This is rendered by
default as a simple solid underline but may be altered using CSS.</td>
</tr>
<tr class="even">
<td><a href="element/var"><code>&lt;var&gt;</code></a></td>
<td>Represents the name of a variable in a mathematical expression or a
programming context. It's typically presented using an italicized
version of the current typeface, although that behavior is
browser-dependent.</td>
</tr>
<tr class="odd">
<td><a href="element/wbr"><code>&lt;wbr&gt;</code></a></td>
<td>Represents a word break opportunity—a position within text where the
browser may optionally break a line, though its line-breaking rules
would not otherwise create a break at that location.</td>
</tr>
</tbody>
</table>

</figure>
:::

## Image and multimedia {#image_and_multimedia}

::: section-content
HTML supports various multimedia resources such as images, audio, and
video.

<figure class="table-container">
<div class="_table">
<table>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element/area"><code>&lt;area&gt;</code></a></td>
<td>Defines an area inside an image map that has predefined clickable
areas. An <em>image map</em> allows geometric areas on an image to be
associated with <a
href="https://developer.mozilla.org/en-US/docs/Glossary/Hyperlink">hyperlink</a>.</td>
</tr>
<tr class="even">
<td><a href="element/audio"><code>&lt;audio&gt;</code></a></td>
<td>Used to embed sound content in documents. It may contain one or more
audio sources, represented using the <code>src</code> attribute or the
source element: the browser will choose the most suitable one. It can
also be the destination for streamed media, using a <a
href="https://developer.mozilla.org/en-US/docs/Web/API/MediaStream"><code>MediaStream</code></a>.</td>
</tr>
<tr class="odd">
<td><a href="element/img"><code>&lt;img&gt;</code></a></td>
<td>Embeds an image into the document.</td>
</tr>
<tr class="even">
<td><a href="element/map"><code>&lt;map&gt;</code></a></td>
<td>Used with <a href="element/area"><code>&lt;area&gt;</code></a>
elements to define an image map (a clickable link area).</td>
</tr>
<tr class="odd">
<td><a href="element/track"><code>&lt;track&gt;</code></a></td>
<td>Used as a child of the media elements, audio and video. It lets you
specify timed text tracks (or time-based data), for example to
automatically handle subtitles. The tracks are formatted in <a
href="https://developer.mozilla.org/en-US/docs/Web/API/WebVTT_API">WebVTT
format</a> (<code>.vtt</code> files)—Web Video Text Tracks.</td>
</tr>
<tr class="even">
<td><a href="element/video"><code>&lt;video&gt;</code></a></td>
<td>Embeds a media player which supports video playback into the
document. You can also use <code>&lt;video&gt;</code> for audio content,
but the audio element may provide a more appropriate user
experience.</td>
</tr>
</tbody>
</table>

</figure>
:::

## Embedded content {#embedded_content}

::: section-content
In addition to regular multimedia content, HTML can include a variety of
other content, even if it\'s not always easy to interact with.

<figure class="table-container">
<div class="_table">
<table>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element/embed"><code>&lt;embed&gt;</code></a></td>
<td>Embeds external content at the specified point in the document. This
content is provided by an external application or other source of
interactive content such as a browser plug-in.</td>
</tr>
<tr class="even">
<td><a href="element/iframe"><code>&lt;iframe&gt;</code></a></td>
<td>Represents a nested browsing context, embedding another HTML page
into the current one.</td>
</tr>
<tr class="odd">
<td><a href="element/object"><code>&lt;object&gt;</code></a></td>
<td>Represents an external resource, which can be treated as an image, a
nested browsing context, or a resource to be handled by a plugin.</td>
</tr>
<tr class="even">
<td><a href="element/picture"><code>&lt;picture&gt;</code></a></td>
<td>Contains zero or more <a
href="element/source"><code>&lt;source&gt;</code></a> elements and one
<a href="element/img"><code>&lt;img&gt;</code></a> element to offer
alternative versions of an image for different display/device
scenarios.</td>
</tr>
<tr class="odd">
<td><a href="element/portal"><code>&lt;portal&gt;</code></a></td>
<td>Enables the embedding of another HTML page into the current one to
enable smoother navigation into new pages.</td>
</tr>
<tr class="even">
<td><a href="element/source"><code>&lt;source&gt;</code></a></td>
<td>Specifies multiple media resources for the picture, the audio
element, or the video element. It is a void element, meaning that it has
no content and does not have a closing tag. It is commonly used to offer
the same media content in multiple file formats in order to provide
compatibility with a broad range of browsers given their differing
support for <a
href="https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types">image
file formats</a> and <a
href="https://developer.mozilla.org/en-US/docs/Web/Media/Formats">media
file formats</a>.</td>
</tr>
</tbody>
</table>

</figure>
:::

## SVG and MathML {#svg_and_mathml}

::: section-content
You can embed [SVG](https://developer.mozilla.org/en-US/docs/Web/SVG)
and [MathML](https://developer.mozilla.org/en-US/docs/Web/MathML)
content directly into HTML documents, using the
[`<svg>`](https://developer.mozilla.org/en-US/docs/Web/SVG/Element/svg)
and
[`<math>`](https://developer.mozilla.org/en-US/docs/Web/MathML/Element/math)
elements.

<figure class="table-container">
<div class="_table">
<table>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/SVG/Element/svg"><code>&lt;svg&gt;</code></a></td>
<td>Container defining a new coordinate system and <a
href="https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/viewBox">viewport</a>.
It is used as the outermost element of SVG documents, but it can also be
used to embed an SVG fragment inside an SVG or HTML document.</td>
</tr>
<tr class="even">
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/MathML/Element/math"><code>&lt;math&gt;</code></a></td>
<td>The top-level element in MathML. Every valid MathML instance must be
wrapped in it. In addition, you must not nest a second
<code>&lt;math&gt;</code> element in another, but you can have an
arbitrary number of other child elements in it.</td>
</tr>
</tbody>
</table>

</figure>
:::

## Scripting

::: section-content
To create dynamic content and Web applications, HTML supports the use of
scripting languages, most prominently JavaScript. Certain elements
support this capability.

<figure class="table-container">
<div class="_table">
<table>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element/canvas"><code>&lt;canvas&gt;</code></a></td>
<td>Container element to use with either the <a
href="https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API">canvas
scripting API</a> or the <a
href="https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API">WebGL
API</a> to draw graphics and animations.</td>
</tr>
<tr class="even">
<td><a href="element/noscript"><code>&lt;noscript&gt;</code></a></td>
<td>Defines a section of HTML to be inserted if a script type on the
page is unsupported or if scripting is currently turned off in the
browser.</td>
</tr>
<tr class="odd">
<td><a href="element/script"><code>&lt;script&gt;</code></a></td>
<td>Used to embed executable code or data; this is typically used to
embed or refer to JavaScript code. The <code>&lt;script&gt;</code>
element can also be used with other languages, such as <a
href="https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API">WebGL</a>'s
GLSL shader programming language and <a
href="https://developer.mozilla.org/en-US/docs/Glossary/JSON">JSON</a>.</td>
</tr>
</tbody>
</table>

</figure>
:::

## Demarcating edits {#demarcating_edits}

::: section-content
These elements let you provide indications that specific parts of the
text have been altered.

<figure class="table-container">
<div class="_table">
<table>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element/del"><code>&lt;del&gt;</code></a></td>
<td>Represents a range of text that has been deleted from a document.
This can be used when rendering "track changes" or source code diff
information, for example. The <code>&lt;ins&gt;</code> element can be
used for the opposite purpose: to indicate text that has been added to
the document.</td>
</tr>
<tr class="even">
<td><a href="element/ins"><code>&lt;ins&gt;</code></a></td>
<td>Represents a range of text that has been added to a document. You
can use the <code>&lt;del&gt;</code> element to similarly represent a
range of text that has been deleted from the document.</td>
</tr>
</tbody>
</table>

</figure>
:::

## Table content {#table_content}

::: section-content
The elements here are used to create and handle tabular data.

<figure class="table-container">
<div class="_table">
<table>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element/caption"><code>&lt;caption&gt;</code></a></td>
<td>Specifies the caption (or title) of a table.</td>
</tr>
<tr class="even">
<td><a href="element/col"><code>&lt;col&gt;</code></a></td>
<td>Defines a column within a table and is used for defining common
semantics on all common cells. It is generally found within a <a
href="element/colgroup"><code>&lt;colgroup&gt;</code></a> element.</td>
</tr>
<tr class="odd">
<td><a href="element/colgroup"><code>&lt;colgroup&gt;</code></a></td>
<td>Defines a group of columns within a table.</td>
</tr>
<tr class="even">
<td><a href="element/table"><code>&lt;table&gt;</code></a></td>
<td>Represents tabular data — that is, information presented in a
two-dimensional table comprised of rows and columns of cells containing
data.</td>
</tr>
<tr class="odd">
<td><a href="element/tbody"><code>&lt;tbody&gt;</code></a></td>
<td>Encapsulates a set of table rows (<a
href="element/tr"><code>&lt;tr&gt;</code></a> elements), indicating that
they comprise the body of the table (<a
href="element/table"><code>&lt;table&gt;</code></a>).</td>
</tr>
<tr class="even">
<td><a href="element/td"><code>&lt;td&gt;</code></a></td>
<td>Defines a cell of a table that contains data. It participates in the
<em>table model</em>.</td>
</tr>
<tr class="odd">
<td><a href="element/tfoot"><code>&lt;tfoot&gt;</code></a></td>
<td>Defines a set of rows summarizing the columns of the table.</td>
</tr>
<tr class="even">
<td><a href="element/th"><code>&lt;th&gt;</code></a></td>
<td>Defines a cell as a header of a group of table cells. The exact
nature of this group is defined by the <code>scope</code> and
<code>headers</code> attributes.</td>
</tr>
<tr class="odd">
<td><a href="element/thead"><code>&lt;thead&gt;</code></a></td>
<td>Defines a set of rows defining the head of the columns of the
table.</td>
</tr>
<tr class="even">
<td><a href="element/tr"><code>&lt;tr&gt;</code></a></td>
<td>Defines a row of cells in a table. The row's cells can then be
established using a mix of <a
href="element/td"><code>&lt;td&gt;</code></a> (data cell) and <a
href="element/th"><code>&lt;th&gt;</code></a> (header cell)
elements.</td>
</tr>
</tbody>
</table>

</figure>
:::

## Forms

::: section-content
HTML provides several elements that can be used together to create forms
that the user can fill out and submit to the website or application.
Further information about this available in the [HTML forms
guide](https://developer.mozilla.org/en-US/docs/Learn/Forms).

<figure class="table-container">
<div class="_table">
<table>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element/button"><code>&lt;button&gt;</code></a></td>
<td>An interactive element activated by a user with a mouse, keyboard,
finger, voice command, or other assistive technology. Once activated, it
performs an action, such as submitting a <a
href="https://developer.mozilla.org/en-US/docs/Learn/Forms">form</a> or
opening a dialog.</td>
</tr>
<tr class="even">
<td><a href="element/datalist"><code>&lt;datalist&gt;</code></a></td>
<td>Contains a set of <a
href="element/option"><code>&lt;option&gt;</code></a> elements that
represent the permissible or recommended options available to choose
from within other controls.</td>
</tr>
<tr class="odd">
<td><a href="element/fieldset"><code>&lt;fieldset&gt;</code></a></td>
<td>Used to group several controls as well as labels (<a
href="element/label"><code>&lt;label&gt;</code></a>) within a web
form.</td>
</tr>
<tr class="even">
<td><a href="element/form"><code>&lt;form&gt;</code></a></td>
<td>Represents a document section containing interactive controls for
submitting information.</td>
</tr>
<tr class="odd">
<td><a href="element/input"><code>&lt;input&gt;</code></a></td>
<td>Used to create interactive controls for web-based forms to accept
data from the user; a wide variety of types of input data and control
widgets are available, depending on the device and user agent. The
<code>&lt;input&gt;</code> element is one of the most powerful and
complex in all of HTML due to the sheer number of combinations of input
types and attributes.</td>
</tr>
<tr class="even">
<td><a href="element/label"><code>&lt;label&gt;</code></a></td>
<td>Represents a caption for an item in a user interface.</td>
</tr>
<tr class="odd">
<td><a href="element/legend"><code>&lt;legend&gt;</code></a></td>
<td>Represents a caption for the content of its parent <a
href="element/fieldset"><code>&lt;fieldset&gt;</code></a>.</td>
</tr>
<tr class="even">
<td><a href="element/meter"><code>&lt;meter&gt;</code></a></td>
<td>Represents either a scalar value within a known range or a
fractional value.</td>
</tr>
<tr class="odd">
<td><a href="element/optgroup"><code>&lt;optgroup&gt;</code></a></td>
<td>Creates a grouping of options within a <a
href="element/select"><code>&lt;select&gt;</code></a> element.</td>
</tr>
<tr class="even">
<td><a href="element/option"><code>&lt;option&gt;</code></a></td>
<td>Used to define an item contained in a select, an <a
href="element/optgroup"><code>&lt;optgroup&gt;</code></a>, or a <a
href="element/datalist"><code>&lt;datalist&gt;</code></a> element. As
such, <code>&lt;option&gt;</code> can represent menu items in popups and
other lists of items in an HTML document.</td>
</tr>
<tr class="odd">
<td><a href="element/output"><code>&lt;output&gt;</code></a></td>
<td>Container element into which a site or app can inject the results of
a calculation or the outcome of a user action.</td>
</tr>
<tr class="even">
<td><a href="element/progress"><code>&lt;progress&gt;</code></a></td>
<td>Displays an indicator showing the completion progress of a task,
typically displayed as a progress bar.</td>
</tr>
<tr class="odd">
<td><a href="element/select"><code>&lt;select&gt;</code></a></td>
<td>Represents a control that provides a menu of options.</td>
</tr>
<tr class="even">
<td><a href="element/textarea"><code>&lt;textarea&gt;</code></a></td>
<td>Represents a multi-line plain-text editing control, useful when you
want to allow users to enter a sizeable amount of free-form text, for
example, a comment on a review or feedback form.</td>
</tr>
</tbody>
</table>

</figure>
:::

## Interactive elements {#interactive_elements}

::: section-content
HTML offers a selection of elements that help to create interactive user
interface objects.

<figure class="table-container">
<div class="_table">
<table>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element/details"><code>&lt;details&gt;</code></a></td>
<td>Creates a disclosure widget in which information is visible only
when the widget is toggled into an "open" state. A summary or label must
be provided using the <a
href="element/summary"><code>&lt;summary&gt;</code></a> element.</td>
</tr>
<tr class="even">
<td><a href="element/dialog"><code>&lt;dialog&gt;</code></a></td>
<td>Represents a dialog box or other interactive component, such as a
dismissible alert, inspector, or subwindow.</td>
</tr>
<tr class="odd">
<td><a href="element/summary"><code>&lt;summary&gt;</code></a></td>
<td>Specifies a summary, caption, or legend for a details element's
disclosure box. Clicking the <code>&lt;summary&gt;</code> element
toggles the state of the parent <a
href="element/details"><code>&lt;details&gt;</code></a> element open and
closed.</td>
</tr>
</tbody>
</table>

</figure>
:::

## Web Components {#web_components}

::: section-content
Web Components is an HTML-related technology that makes it possible to,
essentially, create and use custom elements as if it were regular HTML.
In addition, you can create custom versions of standard HTML elements.

<figure class="table-container">
<div class="_table">
<table>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element/slot"><code>&lt;slot&gt;</code></a></td>
<td>Part of the <a
href="https://developer.mozilla.org/en-US/docs/Web/API/Web_components">Web
Components</a> technology suite, this element is a placeholder inside a
web component that you can fill with your own markup, which lets you
create separate DOM trees and present them together.</td>
</tr>
<tr class="even">
<td><a href="element/template"><code>&lt;template&gt;</code></a></td>
<td>A mechanism for holding HTML that is not to be rendered immediately
when a page is loaded but may be instantiated subsequently during
runtime using JavaScript.</td>
</tr>
</tbody>
</table>

</figure>
:::

## Obsolete and deprecated elements {#obsolete_and_deprecated_elements}

::: section-content
::: {#sect2 .notecard .warning}
**Warning:** These are old HTML elements that are deprecated and should
not be used. **You should never use them in new projects, and you should
replace them in old projects as soon as you can.** They are listed here
for completeness only.
:::

<figure class="table-container">
<div class="_table">
<table>
<thead>
<tr class="header">
<th>Element</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element/acronym"><code>&lt;acronym&gt;</code></a></td>
<td>Allows authors to clearly indicate a sequence of characters that
compose an acronym or abbreviation for a word.</td>
</tr>
<tr class="even">
<td><a href="element/big"><code>&lt;big&gt;</code></a></td>
<td>Renders the enclosed text at a font size one level larger than the
surrounding text (<code>medium</code> becomes <code>large</code>, for
example). The size is capped at the browser's maximum permitted font
size.</td>
</tr>
<tr class="odd">
<td><a href="element/center"><code>&lt;center&gt;</code></a></td>
<td>Displays its block-level or inline contents centered horizontally
within its containing element.</td>
</tr>
<tr class="even">
<td><code>&lt;content&gt;</code></td>
<td>An obsolete part of the <a
href="https://developer.mozilla.org/en-US/docs/Web/API/Web_components">Web
Components</a> suite of technologies—was used inside of <a
href="https://developer.mozilla.org/en-US/docs/Web/API/Web_components/Using_shadow_DOM">Shadow
DOM</a> as an insertion point, and wasn't meant to be used in ordinary
HTML. It has now been replaced by the <a
href="element/slot"><code>&lt;slot&gt;</code></a> element, which creates
a point in the DOM at which a shadow DOM can be inserted. Consider using
<a href="element/slot"><code>&lt;slot&gt;</code></a> instead.</td>
</tr>
<tr class="odd">
<td><a href="element/dir"><code>&lt;dir&gt;</code></a></td>
<td>Container for a directory of files and/or folders, potentially with
styles and icons applied by the user agent. Do not use this obsolete
element; instead, you should use the <a
href="element/ul"><code>&lt;ul&gt;</code></a> element for lists,
including lists of files.</td>
</tr>
<tr class="even">
<td><a href="element/font"><code>&lt;font&gt;</code></a></td>
<td>Defines the font size, color and face for its content.</td>
</tr>
<tr class="odd">
<td><a href="element/frame"><code>&lt;frame&gt;</code></a></td>
<td>Defines a particular area in which another HTML document can be
displayed. A frame should be used within a <a
href="element/frameset"><code>&lt;frameset&gt;</code></a>.</td>
</tr>
<tr class="even">
<td><a href="element/frameset"><code>&lt;frameset&gt;</code></a></td>
<td>Used to contain <a
href="element/frame"><code>&lt;frame&gt;</code></a> elements.</td>
</tr>
<tr class="odd">
<td><a href="element/image"><code>&lt;image&gt;</code></a></td>
<td>An ancient and poorly supported precursor to the <a
href="element/img"><code>&lt;img&gt;</code></a> element. It should not
be used.</td>
</tr>
<tr class="even">
<td><a href="element/marquee"><code>&lt;marquee&gt;</code></a></td>
<td>Used to insert a scrolling area of text. You can control what
happens when the text reaches the edges of its content area using its
attributes.</td>
</tr>
<tr class="odd">
<td><a href="element/menuitem"><code>&lt;menuitem&gt;</code></a></td>
<td>Represents a command that a user is able to invoke through a popup
menu. This includes context menus, as well as menus that might be
attached to a menu button.</td>
</tr>
<tr class="even">
<td><a href="element/nobr"><code>&lt;nobr&gt;</code></a></td>
<td>Prevents the text it contains from automatically wrapping across
multiple lines, potentially resulting in the user having to scroll
horizontally to see the entire width of the text.</td>
</tr>
<tr class="odd">
<td><a href="element/noembed"><code>&lt;noembed&gt;</code></a></td>
<td>An obsolete, non-standard way to provide alternative, or "fallback",
content for browsers that do not support the embed element or do not
support the type of <a
href="content_categories#embedded_content">embedded content</a> an
author wishes to use. This element was deprecated in HTML 4.01 and above
in favor of placing fallback content between the opening and closing
tags of an <a href="element/object"><code>&lt;object&gt;</code></a>
element.</td>
</tr>
<tr class="even">
<td><a href="element/noframes"><code>&lt;noframes&gt;</code></a></td>
<td>Provides content to be presented in browsers that don't support (or
have disabled support for) the <a
href="element/frame"><code>&lt;frame&gt;</code></a> element. Although
most commonly-used browsers support frames, there are exceptions,
including certain special-use browsers including some mobile browsers,
as well as text-mode browsers.</td>
</tr>
<tr class="odd">
<td><a href="element/param"><code>&lt;param&gt;</code></a></td>
<td>Defines parameters for an <a
href="element/object"><code>&lt;object&gt;</code></a> element.</td>
</tr>
<tr class="even">
<td><a href="element/plaintext"><code>&lt;plaintext&gt;</code></a></td>
<td>Renders everything following the start tag as raw text, ignoring any
following HTML. There is no closing tag, since everything after it is
considered raw text.</td>
</tr>
<tr class="odd">
<td><a href="element/rb"><code>&lt;rb&gt;</code></a></td>
<td>Used to delimit the base text component of a ruby annotation, i.e.
the text that is being annotated. One <code>&lt;rb&gt;</code> element
should wrap each separate atomic segment of the base text.</td>
</tr>
<tr class="even">
<td><a href="element/rtc"><code>&lt;rtc&gt;</code></a></td>
<td>Embraces semantic annotations of characters presented in a ruby of
<a href="element/rb"><code>&lt;rb&gt;</code></a> elements used inside of
<a href="element/ruby"><code>&lt;ruby&gt;</code></a> element. <a
href="element/rb"><code>&lt;rb&gt;</code></a> elements can have both
pronunciation (<a href="element/rt"><code>&lt;rt&gt;</code></a>) and
semantic (<a href="element/rtc"><code>&lt;rtc&gt;</code></a>)
annotations.</td>
</tr>
<tr class="odd">
<td><code>&lt;shadow&gt;</code></td>
<td>An obsolete part of the <a
href="https://developer.mozilla.org/en-US/docs/Web/API/Web_components">Web
Components</a> technology suite that was intended to be used as a shadow
DOM insertion point. You might have used it if you have created multiple
shadow roots under a shadow host. Consider using <a
href="element/slot"><code>&lt;slot&gt;</code></a> instead.</td>
</tr>
<tr class="even">
<td><a href="element/strike"><code>&lt;strike&gt;</code></a></td>
<td>Places a strikethrough (horizontal line) over text.</td>
</tr>
<tr class="odd">
<td><a href="element/tt"><code>&lt;tt&gt;</code></a></td>
<td>Creates inline text which is presented using the user agent default
monospace font face. This element was created for the purpose of
rendering text as it would be displayed on a fixed-width display such as
a teletype, text-only screen, or line printer.</td>
</tr>
<tr class="even">
<td><a href="element/xmp"><code>&lt;xmp&gt;</code></a></td>
<td>Renders text between the start and end tags without interpreting the
HTML in between and using a monospaced font. The HTML2 specification
recommended that it should be rendered wide enough to allow 80
characters per line.</td>
</tr>
</tbody>
</table>

</figure>
:::

## See also {#see_also}

::: section-content
-   [`Element`](https://developer.mozilla.org/en-US/docs/Web/API/Element)
    interface
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element){._attribution-link}
:::
