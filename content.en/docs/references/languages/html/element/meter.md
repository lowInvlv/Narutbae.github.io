

# \<meter\>: The HTML Meter element



::: section-content
The `<meter>` [HTML](../index) element represents either a scalar value
within a known range or a fractional value.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<meter\> {#html-demo-meter .output-heading}

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
    <label for="fuel">Fuel level:</label>

    <meter id="fuel" min="0" max="100" low="33" high="66" optimum="80" value="50">at 50/100</meter>
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
labelable content, palpable content.</td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#phrasing_content">Phrasing
content</a>, but there must be no <code>&lt;meter&gt;</code> element
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
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/structural_roles#structural_roles_with_html_equivalents"><code>meter</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>No <code>role</code> permitted</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMeterElement"><code>HTMLMeterElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`value`](#value)

:   The current numeric value. This must be between the minimum and
    maximum values (`min` attribute and `max` attribute) if they are
    specified. If unspecified or malformed, the value is `0`. If
    specified, but not within the range given by the `min` attribute and
    `max` attribute, the value is equal to the nearest end of the range.

    ::: {#sect1 .notecard .note}
    **Note:** Unless the `value` attribute is between `0` and `1`
    (inclusive), the `min` and `max` attributes should define the range
    so that the `value` attribute\'s value is within it.
    :::

[`min`](#min)

:   The lower numeric bound of the measured range. This must be less
    than the maximum value (`max` attribute), if specified. If
    unspecified, the minimum value is `0`.

[`max`](#max)

:   The upper numeric bound of the measured range. This must be greater
    than the minimum value (`min` attribute), if specified. If
    unspecified, the maximum value is `1`.

[`low`](#low)

:   The upper numeric bound of the low end of the measured range. This
    must be greater than the minimum value (`min` attribute), and it
    also must be less than the high value and maximum value (`high`
    attribute and `max` attribute, respectively), if any are specified.
    If unspecified, or if less than the minimum value, the `low` value
    is equal to the minimum value.

[`high`](#high)

:   The lower numeric bound of the high end of the measured range. This
    must be less than the maximum value (`max` attribute), and it also
    must be greater than the low value and minimum value (`low`
    attribute and `min` attribute, respectively), if any are specified.
    If unspecified, or if greater than the maximum value, the `high`
    value is equal to the maximum value.

[`optimum`](#optimum)

:   This attribute indicates the optimal numeric value. It must be
    within the range (as defined by the `min` attribute and `max`
    attribute). When used with the `low` attribute and `high` attribute,
    it gives an indication where along the range is considered
    preferable. For example, if it is between the `min` attribute and
    the `low` attribute, then the lower range is considered preferred.
    The browser may color the meter\'s bar differently depending on
    whether the value is less than or equal to the optimum value.

[`form`](#form)

:   This optional attribute is used to explicitly set a [`<form>`](form)
    owner for the `<meter>` element. If omitted, the `<meter>` is
    associated with its ancestor `<form>` element or the form
    association set by the `form` attribute on another ancestor element,
    such as on a [`<fieldset>`](fieldset), if any. If included, the
    value must be the [`id`](../global_attributes/id) of a `<form>` in
    the same tree.
:::

## Examples

### Simple example {#simple_example}

::: section-content
#### HTML

::: code-example
[html]{.language-name}

``` {signature="ic/tVZIoOKqzf9hhKRU+V8ra719/91AQQw4/Ku9LKO8=" data-language="html"}
<p>
  Heat the oven to <meter min="200" max="500" value="350">350 degrees</meter>.
</p>
```
:::

#### Result

::: {#sect2 .code-example}
::: iframe
:::
:::

On Google Chrome, the resulting meter looks like this:

![A screenshot of the meter element in Google
Chrome](meter-element-in-google.png){width="504"
height="74" loading="lazy"}
:::

### High and Low range example {#high_and_low_range_example}

::: section-content
Note that in this example the [`min`](#min) attribute is omitted. This
is allowed, as it will default to `0`.

#### HTML {#html_2}

::: code-example
[html]{.language-name}

``` {signature="jIuNcu8JP2Is9t87tZGpBrFJgNQ+rzNj1BVdLO/0JiA=" data-language="html"}
<p>
  He got a <meter low="69" high="80" max="100" value="84">B</meter> on the exam.
</p>
```
:::

#### Result {#result_2}

::: {#sect3 .code-example}
::: iframe
:::
:::

On Google Chrome, the resulting meter looks like this:

![red meter in Google
Chrome](meter-element-in-google-red.png){width="498"
height="70" loading="lazy"}
:::

## Specifications

::: _table
  ----------------------------------------------------------------------------------------------------------
  Specification
  ----------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-meter-element]{.small}](https://html.spec.whatwg.org/multipage/form-elements.html#the-meter-element)

  ----------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
              Desktop                                                         Mobile                                                                                   
  ----------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
              Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `meter`     6         ≤18    16        No                  11      6        No                18               16                    11              10.3            1.0
  `form`      6         ≤18    16        No                  11      6        No                18               16                    11              10.3            1.0
  `high`      6         ≤18    16        No                  11      6        No                18               16                    11              10.3            1.0
  `low`       6         ≤18    16        No                  11      6        No                18               16                    11              10.3            1.0
  `max`       6         ≤18    16        No                  11      6        No                18               16                    11              10.3            1.0
  `min`       6         ≤18    16        No                  11      6        No                18               16                    11              10.3            1.0
  `optimum`   6         ≤18    16        No                  11      6        No                18               16                    11              10.3            1.0
  `value`     6         ≤18    16        No                  11      6        No                18               16                    11              10.3            1.0
:::

## See also {#see_also}

::: section-content
-   [`<progress>`](progress)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meter](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meter){._attribution-link}
:::
