

# HTML attribute: min



::: section-content
The `min` attribute defines the minimum value that is acceptable and
valid for the input containing the attribute. If the
[`value`](../element/input#value) of the element is less than this, the
element fails
[validation](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation).
This value must be less than or equal to the value of the `max`
attribute.

Some input types have a default minimum. If the input has no default
minimum and a value is specified for `min` that can\'t be converted to a
valid number (or no minimum value is set), the input has no minimum
value.

It is valid for the input types including:
[date](../element/input/date), [month](../element/input/month),
[week](../element/input/week), [time](../element/input/time),
[datetime-local](../element/input/datetime-local),
[number](../element/input/number) and [range](../element/input/range)
types, and the [`<meter>`](../element/meter) element.
:::

### Syntax

::: section-content
<figure class="table-container">
<div class="_table">
<table class="no-markdown">
<caption>Syntax for <code>min</code> values by input
<code>type</code></caption>
<thead>
<tr class="header">
<th>Input type</th>
<th>Syntax</th>
<th>Example</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="../element/input/date">date</a></td>
<td><code>yyyy-mm-dd</code></td>
<td><code>&lt;input type="date" min="2019-12-25" step="1"&gt;</code></td>
</tr>
<tr class="even">
<td><a href="../element/input/month">month</a></td>
<td><code>yyyy-mm</code></td>
<td><code>&lt;input type="month" min="2019-12" step="12"&gt;</code></td>
</tr>
<tr class="odd">
<td><a href="../element/input/week">week</a></td>
<td><code>yyyy-W##</code></td>
<td><code>&lt;input type="week" min="2019-W23" step=""&gt;</code></td>
</tr>
<tr class="even">
<td><a href="../element/input/time">time</a></td>
<td><code>hh:mm</code></td>
<td><code>&lt;input type="time" min="09:00" step="900"&gt;</code></td>
</tr>
<tr class="odd">
<td><a href="../element/input/datetime-local">datetime-local</a></td>
<td><code>yyyy-mm-ddThh:mm</code></td>
<td><code>&lt;input type="datetime-local" min="2019-12-25T19:30"&gt;</code></td>
</tr>
<tr class="even">
<td><a href="../element/input/number">number</a></td>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/CSS/number">&lt;number&gt;</a></td>
<td><code>&lt;input type="number" min="0" step="5" max="100"&gt;</code></td>
</tr>
<tr class="odd">
<td><a href="../element/input/range">range</a></td>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/CSS/number">&lt;number&gt;</a></td>
<td><code>&lt;input type="range" min="60" step="5" max="100"&gt;</code></td>
</tr>
</tbody>
</table>

</figure>

::: {#sect1 .notecard .note}
**Note:** When the data entered by the user doesn\'t adhere to the min
value set, the value is considered invalid in constraint validation and
will match the
[`:invalid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:invalid)
and
[`:out-of-range`](https://developer.mozilla.org/en-US/docs/Web/CSS/:out-of-range)
pseudo-classes.
:::

See [Client-side validation](../constraint_validation) and
[`rangeUnderflow`](https://developer.mozilla.org/en-US/docs/Web/API/ValidityState/rangeUnderflow)
for more information.

For the [`<meter>`](../element/meter) element, the `min` attribute
defines the lower numeric bound of the measured range. This must be less
than the minimum value ([`max`](max) attribute), if specified. In both
cases, if omitted, the value defaults to 1.

<figure class="table-container">
<div class="_table">
<table class="no-markdown">
<caption>Syntax for <code>min</code> values for other elements</caption>
<thead>
<tr class="header">
<th>Input type</th>
<th>Syntax</th>
<th>Example</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="../element/meter"><code>&lt;meter&gt;</code></a></td>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/CSS/number">&lt;number&gt;</a></td>
<td><code>&lt;meter id="fuel" min="0" max="100" low="33" high="66" optimum="80" value="40"&gt; at 40/100&lt;/meter&gt;</code></td>
</tr>
</tbody>
</table>

</figure>
:::

### Impact on step {#impact_on_step}

::: section-content
The value of `min` and `step` define what are valid values, even if the
`step` attribute is not included, as `step` defaults to `0`.

We add a big red border around invalid inputs:

::: code-example
[css]{.language-name}

``` {signature="6PMEpHs0vkMNWTCDnxCiFvk6vsP7Y36Lf2EE3Y3cOfI=" data-language="css"}
input:invalid {
  border: solid red 3px;
}
```
:::

Then define an input with a minimum value of 7.2, omitting the step
attribute, wherein it defaults to 1.

::: code-example
[html]{.language-name}

``` {signature="IBE0MUa6DsxcbCQLivNNQhubuPsXnlrlV7GbPV/KSVU=" data-language="html"}
<input id="myNumber" name="myNumber" type="number" min="7.2" value="8" />
```
:::

Because `step` defaults to 1, valid values include `7.2`, `8.2`, `9.2`,
and so on. The value 8 is not valid. As we included an invalid value,
supporting browsers will show the value as invalid.

::: {#sect2 .code-example}
::: iframe
:::
:::

If not explicitly included, `step` defaults to 1 for `number` and
`range`, and 1 unit type (second, week, month, day) for the date/time
input types.
:::

## Accessibility concerns {#accessibility_concerns}

::: section-content
Provide instructions to help users understand how to complete the form
and use individual form controls. Indicate any required and optional
input, data formats, and other relevant information. When using the
`min` attribute, ensure this minimum requirement is understood by the
user. Providing instructions within the [`<label>`](../element/label)
may be sufficient. If providing instructions outside of labels, which
allows more flexible positioning and design, consider using
[`aria-labelledby`](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-labelledby)
or
[`aria-describedby`](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-describedby).
:::

## Specifications

::: _table
  --------------------------------------------------------------------------------------------------------------------
  Specification
  --------------------------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-min-and-max-attributes]{.small}](https://html.spec.whatwg.org/multipage/input.html#the-min-and-max-attributes)

  [HTML Standard\
  [\# attr-meter-max]{.small}](https://html.spec.whatwg.org/multipage/form-elements.html#attr-meter-max)
  --------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
          Desktop                                                         Mobile                                                                                   
  ------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
          Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `min`   6         ≤18    16        No                  11      6        No                18               16                    11              10.3            1.0
:::

::: _table
          Desktop                                                         Mobile                                                                                   
  ------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
          Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `min`   4         12     16        10                  ≤12.1   5        ≤37               18               16                    ≤12.1           4               1.0
:::

### html.elements.input.min

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

### html.elements.meter.min

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

## See also {#see_also}

::: section-content
-   [`step`](step)
-   [`max`](max)
-   other meter attributes:
    [`low`](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/low){.page-not-created},
    [`high`](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/high){.page-not-created},
    [`optimum`](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/optimum){.page-not-created}
-   [Constraint validation](../constraint_validation)
-   [Form
    validation](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation)
-   [`validityState.rangeUnderflow`](https://developer.mozilla.org/en-US/docs/Web/API/ValidityState/rangeUnderflow)
-   [`:out-of-range`](https://developer.mozilla.org/en-US/docs/Web/CSS/:out-of-range)
-   [`<input>`](../element/input)
-   [date](../element/input/date), [month](../element/input/month),
    [week](../element/input/week), [time](../element/input/time),
    [datetime-local](../element/input/datetime-local),
    [number](../element/input/number) and
    [range](../element/input/range) types, and the
    [`<meter>`](../element/meter)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/min](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/min){._attribution-link}
:::
