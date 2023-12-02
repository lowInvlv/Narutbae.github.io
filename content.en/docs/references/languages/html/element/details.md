

# \<details\>: The Details disclosure element



::: section-content
The `<details>` [HTML](../index) element creates a disclosure widget in
which information is visible only when the widget is toggled into an
\"open\" state. A summary or label must be provided using the
[`<summary>`](summary) element.

A disclosure widget is typically presented onscreen using a small
triangle which rotates (or twists) to indicate open/closed status, with
a label next to the triangle. The contents of the `<summary>` element
are used as the label for the disclosure widget.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<details\> {#html-demo-details .output-heading}

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
      <summary>Details</summary>
      Something small enough to escape casual notice.
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

A `<details>` widget can be in one of two states. The default *closed*
state displays only the triangle and the label inside `<summary>` (or a
[user
agent](https://developer.mozilla.org/en-US/docs/Glossary/User_agent)-defined
default string if no `<summary>`).

When the user clicks on the widget or focuses it then presses the space
bar, it \"twists\" open, revealing its contents. The common use of a
triangle which rotates or twists around to represent opening or closing
the widget is why these are sometimes called \"twisty\".

You can use CSS to style the disclosure widget, and you can
programmatically open and close the widget by setting/removing its
[`open`](#open) attribute. Unfortunately, at this time, there\'s no
built-in way to animate the transition between open and closed.

By default when closed, the widget is only tall enough to display the
disclosure triangle and summary. When open, it expands to display the
details contained within.

Fully standards-compliant implementations automatically apply the CSS
[`display`](https://developer.mozilla.org/en-US/docs/Web/CSS/display)`: list-item`
to the [`<summary>`](summary) element. You can use this to customize its
appearance further. See [Customizing the disclosure
widget](#customizing_the_disclosure_widget) for further details.
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`open`](#open)

:   This Boolean attribute indicates whether the details --- that is,
    the contents of the `<details>` element --- are currently visible.
    The details are shown when this attribute exists, or hidden when
    this attribute is absent. By default this attribute is absent which
    means the details are not visible.

    ::: {#sect1 .notecard .note}
    **Note:** You have to remove this attribute entirely to make the
    details hidden. `open="false"` makes the details visible because
    this attribute is Boolean.
    :::
:::

## Events

::: section-content
In addition to the usual events supported by HTML elements, the
`<details>` element supports the
[`toggle`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLDetailsElement/toggle_event)
event, which is dispatched to the `<details>` element whenever its state
changes between open and closed. It is sent *after* the state is
changed, although if the state changes multiple times before the browser
can dispatch the event, the events are coalesced so that only one is
sent.

You can use an event listener for the `toggle` event to detect when the
widget changes state:

::: code-example
[js]{.language-name}

``` {signature="uFlpOGna6XagO5ci3kXHaUmvBMME9wNxK9NlxavUmHw=" data-language="js"}
details.addEventListener("toggle", (event) => {
  if (details.open) {
    /* the element was toggled open */
  } else {
    /* the element was toggled closed */
  }
});
```
:::
:::

## Examples

### A simple disclosure example {#a_simple_disclosure_example}

::: section-content
This example shows a simple `<details>` element with a `<summary>`.

::: code-example
[html]{.language-name}

``` {signature="qpItHAkBiYNruaTloJeKVBAtzMB7IFs2eEW8C9MNCk4=" data-language="html"}
<details>
  <summary>System Requirements</summary>
  <p>
    Requires a computer running an operating system. The computer must have some
    memory and ideally some kind of long-term storage. An input device as well
    as some form of output device is recommended.
  </p>
</details>
```
:::

#### Result

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Creating an open disclosure box {#creating_an_open_disclosure_box}

::: section-content
To start the `<details>` box in its open state, add the Boolean `open`
attribute:

::: code-example
[html]{.language-name}

``` {signature="gnBXB28XondnpjuhBrPGz3KCQihbijwV0sBRQCyw1BQ=" data-language="html"}
<details open>
  <summary>System Requirements</summary>
  <p>
    Requires a computer running an operating system. The computer must have some
    memory and ideally some kind of long-term storage. An input device as well
    as some form of output device is recommended.
  </p>
</details>
```
:::

#### Result {#result_2}

::: {#sect3 .code-example}
::: iframe
:::
:::
:::

### Customizing the appearance {#customizing_the_appearance}

::: section-content
Now let\'s apply some CSS to customize the appearance of the disclosure
box.

#### CSS

::: code-example
[css]{.language-name}

``` {signature="UxgN4w/bDU+pIezvMttGx9i4W+PeVMBpygxdZ+MYWx8=" data-language="css"}
details {
  font:
    16px "Open Sans",
    Calibri,
    sans-serif;
  width: 620px;
}

details > summary {
  padding: 2px 6px;
  width: 15em;
  background-color: #ddd;
  border: none;
  box-shadow: 3px 3px 4px black;
  cursor: pointer;
}

details > p {
  border-radius: 0 0 10px 10px;
  background-color: #ddd;
  padding: 2px 6px;
  margin: 0;
  box-shadow: 3px 3px 4px black;
}

details[open] > summary {
  background-color: #ccf;
}
```
:::

This CSS creates a look similar to a tabbed interface, where clicking
the tab opens it to reveal its contents.

The selector `details[open]` can be used to style the element which is
open.

#### HTML

::: code-example
[html]{.language-name}

``` {signature="qpItHAkBiYNruaTloJeKVBAtzMB7IFs2eEW8C9MNCk4=" data-language="html"}
<details>
  <summary>System Requirements</summary>
  <p>
    Requires a computer running an operating system. The computer must have some
    memory and ideally some kind of long-term storage. An input device as well
    as some form of output device is recommended.
  </p>
</details>
```
:::

#### Result {#result_3}

::: {#sect4 .code-example}
::: iframe
:::
:::
:::

### Customizing the disclosure widget {#customizing_the_disclosure_widget}

::: section-content
The disclosure triangle itself can be customized, although this is not
as broadly supported. There are variations in how browsers support this
customization due to experimental implementations as the element was
standardized, so we\'ll have to use multiple approaches for a while.

The [`<summary>`](summary) element supports the
[`list-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style)
shorthand property and its longhand properties, such as
[`list-style-type`](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-type),
to change the disclosure triangle to whatever you choose (usually with
[`list-style-image`](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-image)).
For example, we can remove the disclosure widget icon by setting
`list-style: none`.

#### CSS {#css_2}

::: code-example
[css]{.language-name}

``` {signature="bMx6onZxL5Wkl+TyHYD3ALYHv8/BO0VQ96UMzGgBwpg=" data-language="css"}
details {
  font:
    16px "Open Sans",
    Calibri,
    sans-serif;
  width: 620px;
}

details > summary {
  padding: 2px 6px;
  width: 15em;
  background-color: #ddd;
  border: none;
  box-shadow: 3px 3px 4px black;
  cursor: pointer;
  list-style: none;
}

details > p {
  border-radius: 0 0 10px 10px;
  background-color: #ddd;
  padding: 2px 6px;
  margin: 0;
  box-shadow: 3px 3px 4px black;
}
```
:::

This CSS creates a look similar to a tabbed interface, where activating
the tab expands and opens it to reveal its contents.

#### HTML {#html_2}

::: code-example
[html]{.language-name}

``` {signature="qpItHAkBiYNruaTloJeKVBAtzMB7IFs2eEW8C9MNCk4=" data-language="html"}
<details>
  <summary>System Requirements</summary>
  <p>
    Requires a computer running an operating system. The computer must have some
    memory and ideally some kind of long-term storage. An input device as well
    as some form of output device is recommended.
  </p>
</details>
```
:::

#### Result {#result_4}

::: {#sect5 .code-example}
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
<th scope="row"><a href="../content_categories">Content
categories</a></th>
<td><a href="../content_categories#flow_content">Flow content</a>,
sectioning root, interactive content, palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>One <a href="summary"><code>&lt;summary&gt;</code></a> element
followed by <a href="../content_categories#flow_content">flow
content</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#flow_content">flow content</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/group_role"><code>group</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>No <code>role</code> permitted</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLDetailsElement"><code>HTMLDetailsElement</code></a></td>
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
  the-details-element]{.small}](https://html.spec.whatwg.org/multipage/interactive-elements.html#the-details-element)

  ---------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  --------------------------------------------------------------------------------------------------------------------------------------
              Desktop                                                    Mobile                                               
  ----------- --------- ------ ------------- ---------- ------- -------- --------- --------- ------------- --------- -------- ----------
              Chrome    Edge   Firefox       Internet   Opera   Safari   WebView   Chrome    Firefox for   Opera     Safari   Samsung
                                             Explorer                    Android   Android   Android       Android   on IOS   Internet

  `details`   12        79     49            No         15      6        4.4       18        49            14        6        1.0
                                                                                                                              
                               Before                                                        There is a                       
                               Firefox 57,                                                   bug meaning                      
                               there was a                                                   that                             
                               bug meaning                                                   `<details>`                      
                               that                                                          elements                         
                               `<details>`                                                   can\'t be                        
                               elements                                                      made open by                     
                               can\'t be                                                     default using                    
                               made open by                                                  the `open`                       
                               default using                                                 attribute if                     
                               the `open`                                                    they have a                      
                               attribute if                                                  CSS                              
                               they have a                                                   `animation`                      
                               CSS                                                           active on                        
                               `animation`                                                   them.                            
                               active on                                                                                      
                               them.                                                                                          

  `name`      120       120    No            No         No      No       No        No        No            No        No       No

  `open`      12        79     49            No         15      6        4.4       18        49            14        6        1.0
  --------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [`<summary>`](summary)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details){._attribution-link}
:::
