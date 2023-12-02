

# \<del\>: The Deleted Text element



::: section-content
The `<del>` [HTML](../index) element represents a range of text that has
been deleted from a document. This can be used when rendering \"track
changes\" or source code diff information, for example. The
[`<ins>`](ins) element can be used for the opposite purpose: to indicate
text that has been added to the document.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<del\> {#html-demo-del .output-heading}

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
    <blockquote>
      There is <del>nothing</del> <ins>no code</ins> either good or bad, but <del>thinking</del> <ins>running it</ins> makes
      it so.
    </blockquote>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    del {
      text-decoration: line-through;
      background-color: #fbb;
      color: #555;
    }

    ins {
      text-decoration: none;
      background-color: #d4fcbc;
    }

    blockquote {
      padding-left: 15px;
      border-left: 3px solid #d7d7db;
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

This element is often (but need not be) rendered by applying a
strike-through style to the text.

<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td><a href="../content_categories#phrasing_content">Phrasing
content</a>, <a href="../content_categories#flow_content">flow
content</a>.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a
href="../content_categories#transparent_content_model">Transparent</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#phrasing_content">phrasing content</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/structural_roles#structural_roles_with_html_equivalents"><code>deletion</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>Any</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLModElement"><code>HTMLModElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Attributes

::: section-content
This element\'s attributes include the [global
attributes](../global_attributes).

[`cite`](#cite)

:   A URI for a resource that explains the change (for example, meeting
    minutes).

[`datetime`](#datetime)

:   This attribute indicates the time and date of the change and must be
    a valid date string with an optional time. If the value cannot be
    parsed as a date with an optional time string, the element does not
    have an associated timestamp. For the format of the string without a
    time, see [Date strings](../date_and_time_formats#date_strings). The
    format of the string if it includes both date and time is covered in
    [Local date and time
    strings](../date_and_time_formats#local_date_and_time_strings).
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="G+TZR/OseBOkRke571VojlCMv8p/HEew4Ys3FSjtefo=" data-language="html"}
<p><del>This text has been deleted</del>, here is the rest of the paragraph.</p>
<del><p>This paragraph has been deleted.</p></del>
```
:::
:::

### Result

::: section-content
::: {#sect1 .code-example}
::: iframe
:::
:::
:::

## Accessibility concerns {#accessibility_concerns}

::: section-content
The presence of the `del` element is not announced by most screen
reading technology in its default configuration. It can be made to be
announced by using the CSS
[`content`](https://developer.mozilla.org/en-US/docs/Web/CSS/content)
property, along with the
[`::before`](https://developer.mozilla.org/en-US/docs/Web/CSS/::before)
and
[`::after`](https://developer.mozilla.org/en-US/docs/Web/CSS/::after)
pseudo-elements.

::: code-example
[css]{.language-name}

``` {signature="qGtNqDqqtt1MbQ78KWeowI5a0UodXoXozcv3uLVZfnM=" data-language="css"}
del::before,
del::after {
  clip-path: inset(100%);
  clip: rect(1px, 1px, 1px, 1px);
  height: 1px;
  overflow: hidden;
  position: absolute;
  white-space: nowrap;
  width: 1px;
}

del::before {
  content: " [deletion start] ";
}

del::after {
  content: " [deletion end] ";
}
```
:::

Some people who use screen readers deliberately disable announcing
content that creates extra verbosity. Because of this, it is important
to not abuse this technique and only apply it in situations where not
knowing content has been deleted would adversely affect understanding.

-   [Short note on making your mark (more accessible) \| The Paciello
    Group](https://www.tpgi.com/short-note-on-making-your-mark-more-accessible/){target="_blank"}
-   [Tweaking Text Level Styles \| Adrian
    Roselli](https://adrianroselli.com/2017/12/tweaking-text-level-styles.html){target="_blank"}
:::

## Specifications

::: _table
  ----------------------------------------------------------------------------------------------
  Specification
  ----------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-del-element]{.small}](https://html.spec.whatwg.org/multipage/edits.html#the-del-element)

  ----------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
               Desktop                                                         Mobile                                                                                   
  ------------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
               Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `del`        1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `cite`       1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `datetime`   1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
:::

## See also {#see_also}

::: section-content
-   [`<ins>`](ins) element for insertions into a text
-   [`<s>`](s) element for strikethrough separate from representing
    deletion of text
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/del](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/del){._attribution-link}
:::
