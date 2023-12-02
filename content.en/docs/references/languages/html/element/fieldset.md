

# \<fieldset\>: The Field Set element



::: section-content
The `<fieldset>` [HTML](../index) element is used to group several
controls as well as labels ([`<label>`](label)) within a web form.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<fieldset\> {#html-demo-fieldset .output-heading}

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
    <form>
      <fieldset>
        <legend>Choose your favorite monster</legend>

        <input type="radio" id="kraken" name="monster" value="K" />
        <label for="kraken">Kraken</label><br />

        <input type="radio" id="sasquatch" name="monster" value="S" />
        <label for="sasquatch">Sasquatch</label><br />

        <input type="radio" id="mothman" name="monster" value="M" />
        <label for="mothman">Mothman</label>
      </fieldset>
    </form>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    legend {
      background-color: #000;
      color: #fff;
      padding: 3px 6px;
    }

    input {
      margin: 0.4rem;
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

As the example above shows, the `<fieldset>` element provides a grouping
for a part of an HTML form, with a nested [`<legend>`](legend) element
providing a caption for the `<fieldset>`. It takes few attributes, the
most notable of which are `form`, which can contain the `id` of a
[`<form>`](form) on the same page, allowing you to make the `<fieldset>`
part of that `<form>` even if it is not nested inside it, and
`disabled`, which allows you to disable the `<fieldset>` and all its
contents in one go.
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`disabled`](#disabled)

:   If this Boolean attribute is set, all form controls that are
    descendants of the `<fieldset>`, are disabled, meaning they are not
    editable and won\'t be submitted along with the [`<form>`](form).
    They won\'t receive any browsing events, like mouse clicks or
    focus-related events. By default browsers display such controls
    grayed out. Note that form elements inside the [`<legend>`](legend)
    element won\'t be disabled.

[`form`](#form)

:   This attribute takes the value of the
    [`id`](../global_attributes#id) attribute of a [`<form>`](form)
    element you want the `<fieldset>` to be part of, even if it is not
    inside the form. Please note that usage of this is confusing --- if
    you want the [`<input>`](input) elements inside the `<fieldset>` to
    be associated with the form, you need to use the `form` attribute
    directly on those elements. You can check which elements are
    associated with a form via JavaScript, using
    [`HTMLFormElement.elements`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLFormElement/elements).

[`name`](#name)

:   The name associated with the group.

    ::: {#sect1 .notecard .note}
    **Note:** The caption for the fieldset is given by the first
    [`<legend>`](legend) element nested inside it.
    :::
:::

## Styling with CSS {#styling_with_css}

::: section-content
There are several special styling considerations for `<fieldset>`.

Its
[`display`](https://developer.mozilla.org/en-US/docs/Web/CSS/display)
value is `block` by default, and it establishes a [block formatting
context](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Block_formatting_context).
If the `<fieldset>` is styled with an inline-level `display` value, it
will behave as `inline-block`, otherwise it will behave as `block`. By
default there is a `2px` `groove` border surrounding the contents, and a
small amount of default padding. The element has
[`min-inline-size: min-content`](https://developer.mozilla.org/en-US/docs/Web/CSS/min-inline-size)
by default.

If a [`<legend>`](legend) is present, it is placed over the
`block-start` border. The `<legend>` shrink-wraps, and also establishes
a formatting context. The `display` value is blockified. (For example,
`display: inline` behaves as `block`.)

There will be an anonymous box holding the contents of the `<fieldset>`,
which inherits certain properties from the `<fieldset>`. If the
`<fieldset>` is styled with `display: grid` or `display: inline-grid`,
then the anonymous box will be a grid formatting context. If the
`<fieldset>` is styled with `display: flex` or `display: inline-flex`,
then the anonymous box will be a flex formatting context. Otherwise, it
establishes a block formatting context.

You can feel free to style the `<fieldset>` and `<legend>` in any way
you want to suit your page design.
:::

## Examples

### Simple fieldset {#simple_fieldset}

::: section-content
This example shows a really simple `<fieldset>` example, with a
`<legend>`, and a single control inside it.

::: code-example
[html]{.language-name}

``` {signature="uxxwh/1R8416PsuWyTQliHC7e4bevA/V60DovcMkyms=" data-language="html"}
<form action="#">
  <fieldset>
    <legend>Do you agree?</legend>
    <input type="checkbox" id="chbx" name="agree" value="Yes!" />
    <label for="chbx">I agree</label>
  </fieldset>
</form>
```
:::

#### Result

::: {#sect2 .code-example}
::: iframe
:::
:::
:::

### Disabled fieldset {#disabled_fieldset}

::: section-content
This example shows a disabled `<fieldset>` with two controls inside it.
Note how both the controls are disabled due to being inside a disabled
`<fieldset>`.

::: code-example
[html]{.language-name}

``` {signature="0xXMY4R9KV5WR0S4VO4CuKYRMlG6uUCJPK+louFaS1M=" data-language="html"}
<form action="#">
  <fieldset disabled>
    <legend>Disabled login fieldset</legend>
    
      <label for="name">Name: </label>
      <input type="text" id="name" value="Chris" />
    
    
      <label for="pwd">Archetype: </label>
      <input type="password" id="pwd" value="Wookie" />
    
  </fieldset>
</form>
```
:::

#### Result {#result_2}

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
href="heading_elements#sectioning_root">sectioning root</a>, <a
href="../content_categories#form_listed">listed</a>, <a
href="../content_categories#form-associated_content">form-associated</a>
element, palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td>An optional <a href="legend"><code>&lt;legend&gt;</code></a>
element, followed by flow content.</td>
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
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/radiogroup_role"><code>radiogroup</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/presentation_role"><code>presentation</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/none_role"><code>none</code></a></td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLFieldSetElement"><code>HTMLFieldSetElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ----------------------------------------------------------------------------------------------------------------
  Specification
  ----------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-fieldset-element]{.small}](https://html.spec.whatwg.org/multipage/form-elements.html#the-fieldset-element)

  ----------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
               Desktop                                                                                                                                                                                                                                                                                            Mobile                                                                                                 
  ------------ ------------------------------------ ------------------------------------------------------------------------------------ --------- --------------------------------------------------------------------------------------------------------------------------------------------- ------- -------- ------------------------------------ ------------------------------------ --------- --------- -------- ------------------------------------
               Chrome                               Edge                                                                                 Firefox   Internet Explorer                                                                                                                             Opera   Safari   WebView Android                      Chrome Android                       Firefox   Opera     Safari   Samsung Internet
                                                                                                                                                                                                                                                                                                                                                                                            for       Android   on IOS   
                                                                                                                                                                                                                                                                                                                                                                                            Android                      

  `fieldset`   1                                    12                                                                                   1         Yes                                                                                                                                           ≤15     ≤4       4.4                                  18                                   4         ≤14       ≤3.2     1.0
                                                                                                                                                                                                                                                                                                                                                                                                                         
               Before version 86, this element did  Before version 86, this element did not support `flexbox` and `grid` layouts within                                                                                                                                                                           Before version 86, this element did  Before version 86, this element did                               Before version 14.0, this element
               not support `flexbox` and `grid`     this element. See [bug                                                                                                                                                                                                                                        not support `flexbox` and `grid`     not support `flexbox` and `grid`                                  did not support `flexbox` and `grid`
               layouts within this element. See     4511145](https://developer.microsoft.com/microsoft-edge/platform/issues/4511145/).                                                                                                                                                                            layouts within this element. See     layouts within this element. See                                  layouts within this element. See
               [bug                                                                                                                                                                                                                                                                                               [bug                                 [bug                                                              [bug
               262679](https://crbug.com/262679).                                                                                                                                                                                                                                                                 262679](https://crbug.com/262679).   262679](https://crbug.com/262679).                                262679](https://crbug.com/262679).

  `disabled`   20                                   12                                                                                   4         Yes                                                                                                                                           12      6        4.4                                  25                                   4         12        6        1.5
                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                    Does not work with nested fieldsets. For example:                                              Not all form control descendants of a disabled fieldset are properly disabled in IE11; see IE [bug 817488: input\[type=\'file\'\] not                                                                                                                                 
                                                    `<fieldset disabled><fieldset><!--Still enabled--></fieldset></fieldset>`                      disabled inside disabled fieldset](https://connect.microsoft.com/IE/feedbackdetail/view/817488) and IE [bug 962368: Can still edit                                                                                                                                    
                                                                                                                                                   input\[type=\'text\'\] within                                                                                                                                                                                                                                         
                                                                                                                                                   fieldset\[disabled\]](https://connect.microsoft.com/IE/feedbackdetail/view/962368/can-still-edit-input-type-text-within-fieldset-disabled).                                                                                                                           

  `form`       1                                    12                                                                                   1         Yes                                                                                                                                           15      3        4.4                                  18                                   4         14        2        1.0

  `name`       19                                   12                                                                                   4         Yes                                                                                                                                           15      6        4.4                                  25                                   4         14        6        1.5
  -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   The [`<legend>`](legend) element
-   The [`<input>`](input) element
-   The [`<label>`](label) element
-   The [`<form>`](form) element
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/fieldset](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/fieldset){._attribution-link}
:::
