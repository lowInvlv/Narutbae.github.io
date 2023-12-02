

# \<ins\>: The Inserted Text element



::: section-content
The `<ins>` [HTML](../index) element represents a range of text that has
been added to a document. You can use the [`<del>`](del) element to
similarly represent a range of text that has been deleted from the
document.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<ins\> {#html-demo-ins .output-heading}

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
    <p>“You're late!”</p>
    <del>
      <p>“I apologize for the delay.”</p>
    </del>
    <ins cite="../howtobeawizard.html" datetime="2018-05">
      <p>“A wizard is never late …”</p>
    </ins>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    del,
    ins {
      display: block;
      text-decoration: none;
      position: relative;
    }

    del {
      background-color: #fbb;
    }

    ins {
      background-color: #d4fcbc;
    }

    del::before,
    ins::before {
      position: absolute;
      left: 0.5rem;
      font-family: monospace;
    }

    del::before {
      content: '−';
    }

    ins::before {
      content: '+';
    }

    p {
      margin: 0 1.8rem 0;
      font-family: Georgia, serif;
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
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/structural_roles#structural_roles_with_html_equivalents"><code>insertion</code></a></td>
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
This element includes the [global attributes](../global_attributes).

[`cite`](#cite)

:   This attribute defines the URI of a resource that explains the
    change, such as a link to meeting minutes or a ticket in a
    troubleshooting system.

[`datetime`](#datetime)

:   This attribute indicates the time and date of the change and must be
    a valid date with an optional time string. If the value cannot be
    parsed as a date with an optional time string, the element does not
    have an associated timestamp. For the format of the string without a
    time, see [Format of a valid date
    string](../date_and_time_formats#date_strings). The format of the
    string if it includes both date and time is covered in [Format of a
    valid local date and time
    string](../date_and_time_formats#local_date_and_time_strings).
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="VxGymyPQ4l0mCfd4mrEHLOMjINvPoTA8FpomIgTn5p8=" data-language="html"}
<ins>This text has been inserted</ins>
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
The presence of the `<ins>` element is not announced by most screen
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

``` {signature="gDn3WjYyrnt3XVGrTDw1bDnEgGsHMpXMWM8h9MFRsXo=" data-language="css"}
ins::before,
ins::after {
  clip-path: inset(100%);
  clip: rect(1px, 1px, 1px, 1px);
  height: 1px;
  overflow: hidden;
  position: absolute;
  white-space: nowrap;
  width: 1px;
}

ins::before {
  content: " [insertion start] ";
}

ins::after {
  content: " [insertion end] ";
}
```
:::

Some people who use screen readers deliberately disable announcing
content that creates extra verbosity. Because of this, it is important
to not abuse this technique and only apply it in situations where not
knowing content has been inserted would adversely affect understanding.

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
  the-ins-element]{.small}](https://html.spec.whatwg.org/multipage/edits.html#the-ins-element)

  ----------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
               Desktop                                                         Mobile                                                                                   
  ------------ --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
               Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `ins`        1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
  `cite`       1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
  `datetime`   1         12     1         Yes                 15      3        4.4               18               4                     14              2               1.0
:::

## See also {#see_also}

::: section-content
-   [`<del>`](del) element for marking deletion into a document
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ins](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ins){._attribution-link}
:::
