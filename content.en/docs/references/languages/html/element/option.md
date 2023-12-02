

# \<option\>: The HTML Option element



::: section-content
The `<option>` [HTML](../index) element is used to define an item
contained in a [`<select>`](select), an [`<optgroup>`](optgroup), or a
[`<datalist>`](datalist) element. As such, `<option>` can represent menu
items in popups and other lists of items in an HTML document.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<option\> {#html-demo-option .output-heading}

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
    <label for="pet-select">Choose a pet:</label>

    <select id="pet-select">
      <option value="">--Please choose an option--</option>
      <option value="dog">Dog</option>
      <option value="cat">Cat</option>
      <option value="hamster">Hamster</option>
      <option value="parrot">Parrot</option>
      <option value="spider">Spider</option>
      <option value="goldfish">Goldfish</option>
    </select>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    label {
      font-family: sans-serif;
      font-size: 1rem;
      padding-right: 10px;
    }

    select {
      font-size: 0.9rem;
      padding: 2px 5px;
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
This element includes the [global attributes](../global_attributes).

[`disabled`](#disabled)

:   If this Boolean attribute is set, this option is not checkable.
    Often browsers grey out such control and it won\'t receive any
    browsing event, like mouse clicks or focus-related ones. If this
    attribute is not set, the element can still be disabled if one of
    its ancestors is a disabled [`<optgroup>`](optgroup) element.

[`label`](#label)

:   This attribute is text for the label indicating the meaning of the
    option. If the `label` attribute isn\'t defined, its value is that
    of the element text content.

[`selected`](#selected)

:   If present, this Boolean attribute indicates that the option is
    initially selected. If the `<option>` element is the descendant of a
    [`<select>`](select) element whose [`multiple`](select#multiple)
    attribute is not set, only one single `<option>` of this
    [`<select>`](select) element may have the `selected` attribute.

[`value`](#value)

:   The content of this attribute represents the value to be submitted
    with the form, should this option be selected. If this attribute is
    omitted, the value is taken from the text content of the option
    element.
:::

## Styling with CSS {#styling_with_css}

::: section-content
Styling the `<option>` element is highly limited. Options don\'t inherit
the font set on the parent. In Firefox, only
[`color`](https://developer.mozilla.org/en-US/docs/Web/CSS/color) and
[`background-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color)
can be set, however in Chrome and Safari it\'s not possible to set any
properties. You can find more details about styling in [our guide to
advanced form
styling](https://developer.mozilla.org/en-US/docs/Learn/Forms/Advanced_form_styling).
:::

## Examples

::: section-content
See [`<select>`](select) for examples.
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
<td>None.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>Text, possibly with escaped characters (like
<code>&amp;eacute;</code>).</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>The start tag is mandatory. The end tag is optional if this element
is immediately followed by another <code>&lt;option&gt;</code> element
or an <a href="optgroup"><code>&lt;optgroup&gt;</code></a>, or if the
parent element has no more content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>A <a href="select"><code>&lt;select&gt;</code></a>, an <a
href="optgroup"><code>&lt;optgroup&gt;</code></a> or a <a
href="datalist"><code>&lt;datalist&gt;</code></a> element.</td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/option_role"><code>option</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>No <code>role</code> permitted</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLOptionElement"><code>HTMLOptionElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ------------------------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-option-element]{.small}](https://html.spec.whatwg.org/multipage/form-elements.html#the-option-element)

  ------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
               Desktop                                                                                                       Mobile                                                                    
  ------------ --------- ------ ---------------------------------------------------------------- ---------- ------- -------- --------- --------- ---------------------------------- --------- -------- ----------
               Chrome    Edge   Firefox                                                          Internet   Opera   Safari   WebView   Chrome    Firefox for Android                Opera     Safari   Samsung
                                                                                                 Explorer                    Android   Android                                      Android   on IOS   Internet

  `option`     1         12     1                                                                Yes        15      ≤4       4.4       18        4                                  14        ≤3.2     1.0

  `disabled`   1         12     1                                                                Yes        15      ≤4       4.4       18        4                                  14        ≤3.2     1.0

  `label`      1         12     1                                                                Yes        15      ≤4       4.4       18        4                                  14        ≤3.2     1.0
                                                                                                                                                                                                       
                                \[\"Before 77, Firefox didn\'t display the value of the `label`                                                  Before 77, Firefox didn\'t display                    
                                attribute as option text if element\'s content was empty. See                                                    the value of the `label` attribute                    
                                [bug 40545](https://bugzil.la/40545).\", \"Historically, Firefox                                                 as option text if element\'s                          
                                has allowed keyboard and mouse events to bubble up from the                                                      content was empty. See [bug                           
                                `<option>` element to the parent `<select>` element, although                                                    40545](https://bugzil.la/40545).                      
                                this behavior is inconsistent across many browsers. For better                                                                                                         
                                Web compatibility (and for technical reasons), they will not                                                                                                           
                                bubble up when Firefox is in multi-process mode and the                                                                                                                
                                `<select>` element is displayed as a drop-down list. The                                                                                                               
                                behavior is unchanged if the `<select>` is presented inline and                                                                                                        
                                it has either the `multiple` attribute defined or a `size`                                                                                                             
                                attribute set to more than `1`. Rather than watching `<option>`                                                                                                        
                                elements for events, you should watch for                                                                                                                              
                                [change](https://developer.mozilla.org/docs/Web/Events/change)                                                                                                         
                                events on `<select>`. See [bug                                                                                                                                         
                                1090602](https://bugzil.la/1090602) for details.\", \"When                                                                                                             
                                Mozilla introduced dedicated content threads to Firefox (through                                                                                                       
                                the Electrolysis, or e10s, project), support for styling                                                                                                               
                                `<option>` elements was removed temporarily. Starting in Firefox                                                                                                       
                                54, you can apply foreground and background colors to `<option>`                                                                                                       
                                elements again, using the `color` and `background-color` CSS                                                                                                           
                                properties. See [bug 910022](https://bugzil.la/910022) for more                                                                                                        
                                information. Note that this is still disabled in Linux due to                                                                                                          
                                lack of contrast (see [bug 1338283](https://bugzil.la/1338283)                                                                                                         
                                for progress on this).\"\]                                                                                                                                             

  `selected`   1         12     1                                                                Yes        15      ≤4       4.4       18        4                                  14        ≤3.2     1.0

  `value`      1         12     1                                                                Yes        15      ≤4       4.4       18        4                                  14        ≤3.2     1.0
  ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   Other form-related elements: [`<form>`](form), [`<legend>`](legend),
    [`<label>`](label), [`<button>`](button), [`<select>`](select),
    [`<datalist>`](datalist), [`<optgroup>`](optgroup),
    [`<fieldset>`](fieldset), [`<textarea>`](textarea),
    [`<input>`](input), [`<output>`](output), [`<progress>`](progress)
    and [`<meter>`](meter).
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/option](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/option){._attribution-link}
:::
