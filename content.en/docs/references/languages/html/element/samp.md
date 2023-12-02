

# \<samp\>: The Sample Output element



::: section-content
The `<samp>` [HTML](../index) element is used to enclose inline text
which represents sample (or quoted) output from a computer program. Its
contents are typically rendered using the browser\'s default monospaced
font (such as
[Courier](https://en.wikipedia.org/wiki/Courier_(typeface)){target="_blank"}
or Lucida Console).
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<samp\> {#html-demo-samp .output-heading}

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
    <p>I was trying to boot my computer, but I got this hilarious message:</p>

    <p>
      <samp>Keyboard not found <br />Press F1 to continue</samp>
    </p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    samp {
      font-weight: bold;
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
You can use a CSS rule to override the browser\'s default font face for
the `<samp>` element; however, it\'s possible that the browser\'s
preferences may take precedence over any CSS you specify.

The CSS to override the default font face would look like this:

::: code-example
[css]{.language-name}

``` {signature="Uxw6ThaSsf8ELJtNXLp/NodTL+pg+/PyYbpDm+BUX0s=" data-language="css"}
samp {
  font-family: "Courier";
}
```
:::

::: {#sect1 .notecard .note}
**Note:** If you need an element which will serve as a container for
output generated by your website or app\'s JavaScript code, you should
instead use the [`<output>`](output) element.
:::
:::

## Examples

### Basic example {#basic_example}

::: section-content
In this simple example, a paragraph includes an example of the output of
a program.

::: code-example
[html]{.language-name}

``` {signature="XiIjkvkBVMlSUxZu3prSx0AVs4qF37gU/KvgxN5Y9/Q=" data-language="html"}
<p>
  When the process is complete, the utility will output the text
  <samp>Scan complete. Found <em>N</em> results.</samp> You can then proceed to
  the next step.
</p>
```
:::

#### Result

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Sample output including user input {#sample_output_including_user_input}

::: section-content
You can nest the [`<kbd>`](kbd) element within a `<samp>` block to
present an example that includes text entered by the user. For example,
consider this text presenting a transcript of a Linux (or macOS) console
session:

#### HTML

::: code-example
[html]{.language-name}

``` {signature="7h9Kd8DXpiv0gW4ouR5I4lqxiLlAQhryp2oj5TmkcQI=" data-language="html"}
<pre>
<samp><span class="prompt">mike@interwebz:~$</span> <kbd>md5 -s "Hello world"</kbd>
MD5 ("Hello world") = 3e25960a79dbc69b674cd4ec67a72c62

<span class="prompt">mike@interwebz:~$</span> <span class="cursor">█</span></samp></pre>
```
:::

Note the use of [`<span>`](span) to allow customization of the
appearance of specific portions of the sample text such as the shell
prompts and the cursor. Note also the use of `<kbd>` to represent the
command the user entered at the prompt in the sample text.

#### CSS

The CSS that achieves the appearance we want is:

::: code-example
[css]{.language-name}

``` {signature="FJYp9Hh/WyPQU8y6IFO1AgNTQsNF00LXnOuQB/rkqwg=" data-language="css"}
.prompt {
  color: #b00;
}

samp > kbd {
  font-weight: bold;
}

.cursor {
  color: #00b;
}
```
:::

This gives the prompt and cursor fairly subtle colorization and
emboldens the keyboard input within the sample text.

#### Result {#result_2}

The resulting output is this:

::: {#sect3 .code-example}
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
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/generic_role"><code>generic</code></a></td>
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
  ---------------------------------------------------------------------------------------------------------------
  Specification
  ---------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-samp-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-samp-element)

  ---------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
           Desktop                                                         Mobile                                                                                   
  -------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
           Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `samp`   1         12     1         Yes                 15      ≤4       4.4               18               4                     14              ≤3.2            1.0
:::

## See also {#see_also}

::: section-content
-   Related elements: [`<kbd>`](kbd), [`<code>`](code), [`<pre>`](pre)
-   The [`<output>`](output) element: a container for script-generated
    output
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/samp](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/samp){._attribution-link}
:::