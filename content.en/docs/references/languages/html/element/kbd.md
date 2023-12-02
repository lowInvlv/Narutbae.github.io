

# \<kbd\>: The Keyboard Input element



::: section-content
The `<kbd>` [HTML](../index) element represents a span of inline text
denoting textual user input from a keyboard, voice input, or any other
text entry device. By convention, the [user
agent](https://developer.mozilla.org/en-US/docs/Glossary/User_agent)
defaults to rendering the contents of a `<kbd>` element using its
default monospace font, although this is not mandated by the HTML
standard.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<kbd\> {#html-demo-kbd .output-heading}

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
    <p>Please press <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>R</kbd> to re-render an MDN page.</p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    kbd {
      background-color: #eee;
      border-radius: 3px;
      border: 1px solid #b4b4b4;
      box-shadow:
        0 1px 1px rgba(0, 0, 0, 0.2),
        0 2px 0 0 rgba(255, 255, 255, 0.7) inset;
      color: #333;
      display: inline-block;
      font-size: 0.85em;
      font-weight: 700;
      line-height: 1;
      padding: 2px 4px;
      white-space: nowrap;
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

`<kbd>` may be nested in various combinations with the [`<samp>`](samp)
(Sample Output) element to represent various forms of input or output
based on visual cues.
:::

## Attributes

::: section-content
This element only includes the [global
attributes](../global_attributes).
:::

## Usage notes {#usage_notes}

::: section-content
Other elements can be used in tandem with `<kbd>` to represent more
specific scenarios:

-   Nesting a `<kbd>` element within another `<kbd>` element represents
    an actual key or other unit of input as a portion of a larger input.
    See [Representing keystrokes within an
    input](#representing_keystrokes_within_an_input) below.
-   Nesting a `<kbd>` element inside a [`<samp>`](samp) element
    represents input that has been echoed back to the user by the
    system. See [Echoed input](#echoed_input), below, for an example.
-   Nesting a `<samp>` element inside a `<kbd>` element, on the other
    hand, represents input which is based on text presented by the
    system, such as the names of menus and menu items, or the names of
    buttons displayed on the screen. See the example under [Representing
    onscreen input options](#representing_onscreen_input_options) below.

::: {#sect1 .notecard .note}
**Note:** You can define a custom style to override the browser\'s
default font selection for the `<kbd>` element, although the user\'s
preferences may potentially override your CSS.
:::
:::

## Examples

### Basic example {#basic_example}

::: section-content
::: code-example
[html]{.language-name}

``` {signature="ZTbJWrxjhMASwIKNqsUzw1VN/1q19gU28u3tFqRG3Tc=" data-language="html"}
<p>
  Use the command <kbd>help mycommand</kbd> to view documentation for the
  command "mycommand".
</p>
```
:::

#### Result

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Representing keystrokes within an input {#representing_keystrokes_within_an_input}

::: section-content
To describe an input comprised of multiple keystrokes, you can nest
multiple `<kbd>` elements, with an outer `<kbd>` element representing
the overall input and each individual keystroke or component of the
input enclosed within its own `<kbd>`.

#### Unstyled

First, let\'s look at what this looks like as just plain HTML.

##### HTML

::: code-example
[html]{.language-name}

``` {signature="oe7Eg5nq/4f2N2ClXNhbh2ayCMAdOD/XhxFvckYUGIQ=" data-language="html"}
<p>
  You can also create a new document using the
  <kbd><kbd>Ctrl</kbd>+<kbd>N</kbd></kbd> keyboard shortcut.
</p>
```
:::

This wraps the entire key sequence in an outer `<kbd>` element, then
each individual key within its own, in order to denote the components of
the sequence.

::: {#sect3 .notecard .note}
**Note:** You don\'t need to do all this wrapping; you can choose to
simplify it by leaving out the external `<kbd>` element. In other words,
simplifying this to just `<kbd>Ctrl</kbd>+<kbd>N</kbd>` would be
perfectly valid.

**Note:** Depending on your style sheet, though, you may find it useful
to do this kind of nesting.
:::

##### Result {#result_2}

The output looks like this without a style sheet applied:

::: {#sect4 .code-example}
::: iframe
:::
:::

#### With custom styles {#with_custom_styles}

We can make more sense of this by adding some CSS:

##### CSS

We add a new selector for nested `<kbd>` elements, `kbd>kbd`, which we
can apply when rendering keyboard keys:

::: code-example
[css]{.language-name}

``` {signature="j4kW4UyXh7LB9+a8To58tlJDnnfToFHmAdME8bdQoUU=" data-language="css"}
kbd > kbd {
  border-radius: 3px;
  padding: 1px 2px 0;
  border: 1px solid black;
}
```
:::

##### HTML {#html_2}

Then we update the HTML to use this class on the keys in the output to
be presented:

::: code-example
[html]{.language-name}

``` {signature="XBK2d3K2sEkLYg/1BEf54GdKIyEnnx1NmL6ibyAdKh0=" data-language="html"}
<p>
  You can also create a new document by pressing the
  <kbd><kbd>Ctrl</kbd>+<kbd>N</kbd></kbd> shortcut.
</p>
```
:::

##### Result {#result_3}

The result is just what we want!

::: {#sect5 .code-example}
::: iframe
:::
:::
:::

### Echoed input {#echoed_input}

::: section-content
Nesting a `<kbd>` element inside a [`<samp>`](samp) element represents
input that has been echoed back to the user by the system.

::: code-example
[html]{.language-name}

``` {signature="cRO5xElsOic3+L7b0b/PK7++zE4J+KaQWog5Hs9cA8k=" data-language="html"}
<p>
  If a syntax error occurs, the tool will output the initial command you typed
  for your review:
</p>
<blockquote>
  <samp><kbd>custom-git ad my-new-file.cpp</kbd></samp>
</blockquote>
```
:::

#### Result {#result_4}

::: {#sect6 .code-example}
::: iframe
:::
:::
:::

### Representing onscreen input options {#representing_onscreen_input_options}

::: section-content
Nesting a `<samp>` element inside a `<kbd>` element represents input
which is based on text presented by the system, such as the names of
menus and menu items, or the names of buttons displayed on the screen.

For example, you can explain how to choose the \"New Document\" option
in the \"File\" menu using HTML that looks like this:

::: code-example
[html]{.language-name}

``` {signature="g9Fuxj2PJB83TkidSQozMyepKdHCiVYO/ZYRZ5GqlaI=" data-language="html"}
<p>
  To create a new file, choose the <kbd><kbd><samp>File</samp></kbd>
  ⇒<kbd><samp>New Document</samp></kbd></kbd> menu option.
</p>

<p>
  Don't forget to click the <kbd><samp>OK</samp></kbd> button to confirm once
  you've entered the name of the new file.
</p>
```
:::

This does some interesting nesting. For the menu option description, the
entire input is enclosed in a `<kbd>` element. Then, inside that, both
the menu and menu item names are contained within both `<kbd>` and
`<samp>`, indicating an input which is selected from a screen widget.

#### Result {#result_5}

::: {#sect7 .code-example}
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
<td><a href="../content_categories#flow_content">Flow content</a>, <a
href="../content_categories#phrasing_content">phrasing content</a>,
palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#phrasing_content">Phrasing
content</a>.</td>
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
<td><a href="https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role"
target="_blank">No corresponding role</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>Any</td>
</tr>
<tr class="odd">
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
  -------------------------------------------------------------------------------------------------------------
  Specification
  -------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-kbd-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-kbd-element)

  -------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ------------------------------------------------------------------------------------------------------------------------------------
          Desktop                                                          Mobile                                           
  ------- --------- ------ ------------------- ---------- ------- -------- --------- --------- --------- --------- -------- ----------
          Chrome    Edge   Firefox             Internet   Opera   Safari   WebView   Chrome    Firefox   Opera     Safari   Samsung
                                               Explorer                    Android   Android   for       Android   on IOS   Internet
                                                                                               Android                      

  `kbd`   1         12     1                   Yes        15      ≤4       4.4       18        4         14        ≤3.2     1.0
                                                                                                                            
                           Before Firefox 4,                                                                                
                           creating a \<kbd\>                                                                               
                           element incorrectly                                                                              
                           resulted in an                                                                                   
                           `HTMLSpanElement`                                                                                
                           object, instead of                                                                               
                           the expected                                                                                     
                           `HTMLElement`.                                                                                   
  ------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [`<code>`](code)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/kbd](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/kbd){._attribution-link}
:::
