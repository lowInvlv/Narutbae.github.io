

# \<progress\>: The Progress Indicator element



::: section-content
The `<progress>` [HTML](../index) element displays an indicator showing
the completion progress of a task, typically displayed as a progress
bar.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<progress\> {#html-demo-progress .output-heading}

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
    <label for="file">File progress:</label>

    <progress id="file" max="100" value="70">70%</progress>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    label {
      padding-right: 10px;
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
<td><a href="../content_categories#flow_content">Flow content</a>, <a
href="../content_categories#phrasing_content">phrasing content</a>,
labelable content, <a
href="../content_categories#palpable_content">palpable content</a>.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#phrasing_content">Phrasing
content</a>, but there must be no <code>&lt;progress&gt;</code> element
among its descendants.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/progressbar_role"><code>progressbar</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>No <code>role</code> permitted</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLProgressElement"><code>HTMLProgressElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`max`](#max)

:   This attribute describes how much work the task indicated by the
    `progress` element requires. The `max` attribute, if present, must
    have a value greater than `0` and be a valid floating point number.
    The default value is `1`.

[`value`](#value)

:   This attribute specifies how much of the task that has been
    completed. It must be a valid floating point number between `0` and
    `max`, or between `0` and `1` if `max` is omitted. If there is no
    `value` attribute, the progress bar is indeterminate; this indicates
    that an activity is ongoing with no indication of how long it is
    expected to take.

::: {#sect1 .notecard .note}
**Note:** Unlike the [`<meter>`](meter) element, the minimum value is
always 0, and the `min` attribute is not allowed for the `<progress>`
element.
:::

::: {#sect2 .notecard .note}
**Note:** The
[`:indeterminate`](https://developer.mozilla.org/en-US/docs/Web/CSS/:indeterminate)
pseudo-class can be used to match against indeterminate progress bars.
To change the progress bar to indeterminate after giving it a value you
must remove the value attribute with
[`element.removeAttribute('value')`](https://developer.mozilla.org/en-US/docs/Web/API/Element/removeAttribute).
:::
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="sYbVDP2IuhmHL5r75JnUEJV1DgBWTyk+r2Q6Dq4Gv/k=" data-language="html"}
<progress value="70" max="100">70 %</progress>
```
:::
:::

### Result

::: section-content
::: {#sect3 .code-example}
::: iframe
:::
:::
:::

## Accessibility Concerns {#accessibility_concerns}

### Labelling

::: section-content
In most cases you should provide an accessible label when using
`<progress>`. While you can use the standard ARIA labelling attributes
[`aria-labelledby`](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-labelledby)
or
[`aria-label`](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-label)
as you would for any element with `role="progressbar"`, when using
`<progress>` you can alternatively use the [`<label>`](label) element.

::: {#sect4 .notecard .note}
**Note:** Text placed between the element\'s tags is not an accessible
label, it is only recommended as a fallback for old browsers that do not
support this element.
:::

#### Examples {#examples_2}

::: code-example
[html]{.language-name}

``` {signature="2XAw33ZFo8U002wNEFxdJAJJuVI1wG+/0ADjGgbznU8=" data-language="html"}
<label>
  Uploading Document: <progress value="70" max="100">70 %</progress>
</label>

<!-- OR -->
<br />

<label for="progress-bar">Uploading Document</label>
<progress id="progress-bar" value="70" max="100">70 %</progress>
```
:::

#### Result {#result_2}

::: {#sect5 .code-example}
::: iframe
:::
:::
:::

### Describing a particular region {#describing_a_particular_region}

::: section-content
If the `<progress>` element is describing the loading progress of a
section of a page, use
[`aria-describedby`](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-describedby)
to point to the status, and set
[`aria-busy="true"`](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-busy)
on the section that is being updated, removing the `aria-busy` attribute
when it has finished loading.

#### Examples {#examples_3}

::: code-example
[html]{.language-name}

``` {signature="SZbOj87Ct/1GbidII73AYhoOcTVKoCoKk2+TBmURn64=" data-language="html"}
<div aria-busy="true" aria-describedby="progress-bar">
  <!-- content is for this region is loading -->


<!-- ... -->

<progress id="progress-bar" aria-label="Content loading…"></progress>
```
:::

##### Result {#result_3}

::: {#sect6 .code-example}
::: iframe
:::
:::
:::

## Specifications

::: _table
  ----------------------------------------------------------------------------------------------------------------
  Specification
  ----------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-progress-element]{.small}](https://html.spec.whatwg.org/multipage/form-elements.html#the-progress-element)

  ----------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ------------------------------------------------------------------------------------------------------------------------------------------------------------------
               Desktop                                                              Mobile                                                                
  ------------ --------- ------ ----------------------- ---------- ------- -------- --------- --------- ----------------------- --------- --------------- ----------
               Chrome    Edge   Firefox                 Internet   Opera   Safari   WebView   Chrome    Firefox for Android     Opera     Safari on IOS   Samsung
                                                        Explorer                    Android   Android                           Android                   Internet

  `progress`   6         12     6                       10         11      6        4.4       18        6                       11        7               1.0
                                                                                                                                                          
                                \[\"Before Firefox 14,                                                  \[\"Before Firefox 14,            Safari on iOS   
                                the `<progress>`                                                        the `<progress>`                  does not        
                                element was incorrectly                                                 element was incorrectly           support         
                                classified as a form                                                    classified as a form              indeterminate   
                                element, and therefore                                                  element, and therefore            progress bars   
                                had a `form` attribute.                                                 had a `form` attribute.           (they are       
                                This has been fixed.\",                                                 This has been fixed.\",           rendered like   
                                \"Firefox provides the                                                  \"Firefox provides the            0%-completed    
                                `::-moz-progress-bar`                                                   `::-moz-progress-bar`             progress bars). 
                                pseudo-element, which                                                   pseudo-element, which                             
                                lets you style the part                                                 lets you style the part                           
                                of the interior of the                                                  of the interior of the                            
                                progress bar                                                            progress bar                                      
                                representing the amount                                                 representing the amount                           
                                of work completed so                                                    of work completed so                              
                                far.\"\]                                                                far.\"\]                                          

  `max`        6         12     6                       10         11      6        4.4       18        6                       11        7               1.0

  `value`      6         12     6                       10         11      6        4.4       18        6                       11        7               1.0
  ------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [`<meter>`](meter)
-   [`:indeterminate`](https://developer.mozilla.org/en-US/docs/Web/CSS/:indeterminate)
-   [`-moz-orient`](https://developer.mozilla.org/en-US/docs/Web/CSS/-moz-orient)
-   [`::-moz-progress-bar`](https://developer.mozilla.org/en-US/docs/Web/CSS/::-moz-progress-bar)
-   [`::-webkit-progress-bar`](https://developer.mozilla.org/en-US/docs/Web/CSS/::-webkit-progress-bar)
-   [`::-webkit-progress-value`](https://developer.mozilla.org/en-US/docs/Web/CSS/::-webkit-progress-value)
-   [`::-webkit-progress-inner-element`](https://developer.mozilla.org/en-US/docs/Web/CSS/::-webkit-progress-inner-element)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/progress](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/progress){._attribution-link}
:::
