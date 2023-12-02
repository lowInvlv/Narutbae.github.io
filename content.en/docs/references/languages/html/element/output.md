

# \<output\>: The Output element



::: section-content
The `<output>` [HTML](../index) element is a container element into
which a site or app can inject the results of a calculation or the
outcome of a user action.
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`for`](#for)

:   A space-separated list of other elements\'
    [`id`](../global_attributes#id)s, indicating that those elements
    contributed input values to (or otherwise affected) the calculation.

[`form`](#form)

:   The [`<form>`](form) element to associate the output with (its *form
    owner*). The value of this attribute must be the
    [`id`](../global_attributes#id) of a `<form>` in the same document.
    (If this attribute is not set, the `<output>` is associated with its
    ancestor `<form>` element, if any.)

    This attribute lets you associate `<output>` elements to `<form>`s
    anywhere in the document, not just inside a `<form>`. It can also
    override an ancestor `<form>` element.

[`name`](#name)

:   The element\'s name. Used in the
    [`form.elements`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLFormElement/elements)
    API.

The `<output>` value, name, and contents are NOT submitted during form
submission.
:::

## Examples

::: section-content
In the following example, the form provides a slider whose value can
range between `0` and `100`, and an [`<input>`](input) element into
which you can enter a second number. The two numbers are added together,
and the result is displayed in the `<output>` element each time the
value of any of the controls changes.

::: code-example
[html]{.language-name}

``` {signature="E8BAOuvk/mX5mUmJ+nS516ASOd04vytU8mgzgZvVsvo=" data-language="html"}
<form oninput="result.value=parseInt(a.value)+parseInt(b.value)">
  <input type="range" id="b" name="b" value="50" /> +
  <input type="number" id="a" name="a" value="10" /> =
  <output name="result" for="a b">60</output>
</form>
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

## Accessibility Concerns {#accessibility_concerns}

::: section-content
Many browsers implement this element as an
[`aria-live`](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Live_Regions)
region. Assistive technology will thereby announce the results of UI
interactions posted inside it without requiring that focus is switched
away from the controls that produce those results.
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
href="../content_categories#phrasing_content">phrasing content</a>, <a
href="../content_categories#form_listed">listed</a>, <a
href="../content_categories#form_labelable">labelable</a>, <a
href="../content_categories#form_resettable">resettable</a> <a
href="../content_categories#form-associated_content">form-associated
element</a>, palpable content.</td>
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
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/status_role"><code>status</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>Any</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLOutputElement"><code>HTMLOutputElement</code></a></td>
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
  the-output-element]{.small}](https://html.spec.whatwg.org/multipage/form-elements.html#the-output-element)

  ------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
             Desktop                                                         Mobile                                                                                   
  ---------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
             Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `output`   10        ≤18    4         No                  11      7        4.4               18               4                     11              7               1.0
  `for`      10        ≤18    4         No                  11      7        4.4               18               4                     11              7               1.0
  `form`     10        ≤18    4         No                  11      7        4.4               18               4                     11              7               1.0
  `name`     10        ≤18    4         No                  11      7        4.4               18               4                     11              7               1.0
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/output](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/output){._attribution-link}
:::
