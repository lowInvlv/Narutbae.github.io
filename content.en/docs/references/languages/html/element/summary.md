

# \<summary\>: The Disclosure Summary element



::: section-content
The `<summary>` [HTML](../index) element specifies a summary, caption,
or legend for a [`<details>`](details) element\'s disclosure box.
Clicking the `<summary>` element toggles the state of the parent
`<details>` element open and closed.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<summary\> {#html-demo-summary .output-heading}

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
    <details>
      <summary>I have keys but no doors. I have space but no room. You can enter but can’t leave. What am I?</summary>
      A keyboard.
    </details>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    details {
      border: 1px solid #aaa;
      border-radius: 4px;
      padding: 0.5em 0.5em 0;
    }

    summary {
      font-weight: bold;
      margin: -0.5em -0.5em 0;
      padding: 0.5em;
    }

    details[open] {
      padding: 0.5em;
    }

    details[open] summary {
      border-bottom: 1px solid #aaa;
      margin-bottom: 0.5em;
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

## Attributes

::: section-content
This element only includes the [global
attributes](../global_attributes).
:::

## Usage notes {#usage_notes}

::: section-content
The `<summary>` element\'s contents can be any heading content, plain
text, or HTML that can be used within a paragraph.

A `<summary>` element may *only* be used as the first child of a
`<details>` element. When the user clicks on the summary, the parent
`<details>` element is toggled open or closed, and then a
[`toggle`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLDetailsElement/toggle_event)
event is sent to the `<details>` element, which can be used to let you
know when this state change occurs.
:::

### Default label text {#default_label_text}

::: section-content
If a `<details>` element\'s first child is not a `<summary>` element,
the [user
agent](https://developer.mozilla.org/en-US/docs/Glossary/User_agent)
will use a default string (typically \"Details\") as the label for the
disclosure box.
:::

### Default style {#default_style}

::: section-content
Per the HTML specification, the default style for `<summary>` elements
includes `display: list-item`. This makes it possible to change or
remove the icon displayed as the disclosure widget next to the label
from the default, which is typically a triangle.

You can also change the style to `display: block` to remove the
disclosure triangle.

See the [Browser compatibility](#browser_compatibility) section for
details, as not all browsers support full functionality of this element
yet.

For Webkit-based browsers, such as Safari, it is possible to control the
icon display through the non-standard CSS pseudo-element
`::-webkit-details-marker`. To remove the disclosure triangle, use
`summary::-webkit-details-marker { display: none }`.
:::

## Examples

::: section-content
Below are some examples showing `<summary>` in use. You can find more
examples in the documentation for the [`<details>`](details) element.
:::

### Basic example {#basic_example}

::: section-content
A simple example showing the use of `<summary>` in a
[`<details>`](details) element:

::: code-example
[html]{.language-name}

``` {signature="HOi2ZMwsCOmar8ZW4jXf0UP8OWDhVzDcw+qVxj+nsTc=" data-language="html"}
<details open>
  <summary>Overview</summary>
  <ol>
    <li>Cash on hand: $500.00</li>
    <li>Current invoice: $75.30</li>
    <li>Due date: 5/6/19</li>
  </ol>
</details>
```
:::

#### Result

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

### Summaries as headings {#summaries_as_headings}

::: section-content
You can use heading elements in `<summary>`, like this:

::: code-example
[html]{.language-name}

``` {signature="QYs9cS9qT5lDdKD90eqaZI0990MugbN0Xcb3s1Q9vCo=" data-language="html"}
<details open>
  <summary><h4>Overview</h4></summary>
  <ol>
    <li>Cash on hand: $500.00</li>
    <li>Current invoice: $75.30</li>
    <li>Due date: 5/6/19</li>
  </ol>
</details>
```
:::

#### Result {#result_2}

::: {#sect2 .code-example}
::: iframe
:::
:::

This currently has some spacing issues that could be addressed using
CSS.

::: {#sect3 .notecard .warning}
**Warning:** Because the `<summary>` element has a default role of
[button](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/button_role)
(which strips all roles from child elements), this example will not work
for users of assistive technologies such as screen readers. The `<h4>`
will have its role removed and thus will not be treated as a heading for
these users.
:::
:::

### HTML in summaries {#html_in_summaries}

::: section-content
This example adds some semantics to the `<summary>` element to indicate
the label as important:

::: code-example
[html]{.language-name}

``` {signature="Kcy7ZpB8/IzP+mSsQnLGfXDvAVyBzhM22Y1FtipSovk=" data-language="html"}
<details open>
  <summary><strong>Overview</strong></summary>
  <ol>
    <li>Cash on hand: $500.00</li>
    <li>Current invoice: $75.30</li>
    <li>Due date: 5/6/19</li>
  </ol>
</details>
```
:::

#### Result {#result_3}

::: {#sect4 .code-example}
::: iframe
:::
:::
:::

## Technical summary {#technical_summary}

::: section-content
<figure class="table-container">
<div class="_table">
<table class="properties">
<tbody>
<tr class="odd">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#phrasing_content">Phrasing
content</a> or one element of <a
href="../content_categories#heading_content">Heading content</a></td>
</tr>
<tr class="even">
<th scope="row">Tag omission</th>
<td>None; both the start tag and the end tag are mandatory.</td>
</tr>
<tr class="odd">
<th scope="row">Permitted parents</th>
<td>The <a href="details"><code>&lt;details&gt;</code></a> element.</td>
</tr>
<tr class="even">
<th scope="row">Implicit ARIA role</th>
<td><a href="https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role"
target="_blank">No corresponding role</a></td>
</tr>
<tr class="odd">
<th scope="row">Permitted ARIA roles</th>
<td>No <code>role</code> permitted</td>
</tr>
<tr class="even">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement"><code>HTMLElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ---------------------------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-summary-element]{.small}](https://html.spec.whatwg.org/multipage/interactive-elements.html#the-summary-element)

  ---------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
                        Desktop                                                         Mobile                                                                                   
  --------------------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
                        Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `summary`             12        79     49        No                  15      6        4                 18               49                    14              6               1.0
  `display_list_item`   89        89     49        No                  75      No       89                89               49                    63              No              15.0
:::

## See also {#see_also}

::: section-content
-   [`<details>`](details)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/summary](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/summary){._attribution-link}
:::
