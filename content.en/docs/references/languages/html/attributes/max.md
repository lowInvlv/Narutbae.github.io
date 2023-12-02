

# HTML attribute: max



::: section-content
The `max` attribute defines the maximum value that is acceptable and
valid for the input containing the attribute. If the
[`value`](../element/input#value) of the element is greater than this,
the element fails
[validation](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation).
This value must be greater than or equal to the value of the
[`min`](min) attribute. If the `max` attribute is present but is not
specified or is invalid, no `max` value is applied. If the `max`
attribute is valid and a non-empty value is greater than the maximum
allowed by the `max` attribute, constraint validation will prevent form
submission.

Valid for the numeric input types, including the
[date](../element/input/date), [month](../element/input/month),
[week](../element/input/week), [time](../element/input/time),
[datetime-local](../element/input/datetime-local),
[number](../element/input/number) and [range](../element/input/range)
types, and both the [`<progress>`](../element/progress) and
[`<meter>`](../element/meter) elements, the `max` attribute is a number
that specifies the most positive value a form control to be considered
valid.

If the value exceeds the max value allowed, the
[`validityState.rangeOverflow`](https://developer.mozilla.org/en-US/docs/Web/API/ValidityState/rangeOverflow)
will be true, and the control will be matched by the
[`:out-of-range`](https://developer.mozilla.org/en-US/docs/Web/CSS/:out-of-range)
and
[`:invalid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:invalid)
pseudo-classes.
:::

### Syntax

::: section-content
<figure class="table-container">
<div class="_table">
<table class="no-markdown">
<caption>Syntax for <code>max</code> values by input
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
<td><code>&lt;input type="date" max="2019-12-25" step="1"&gt;</code></td>
</tr>
<tr class="even">
<td><a href="../element/input/month">month</a></td>
<td><code>yyyy-mm</code></td>
<td><code>&lt;input type="month" max="2019-12" step="12"&gt;</code></td>
</tr>
<tr class="odd">
<td><a href="../element/input/week">week</a></td>
<td><code>yyyy-W##</code></td>
<td><code>&lt;input type="week" max="2019-W23" step=""&gt;</code></td>
</tr>
<tr class="even">
<td><a href="../element/input/time">time</a></td>
<td><code>hh:mm</code></td>
<td><code>&lt;input type="time" max="17:00" step="900"&gt;</code></td>
</tr>
<tr class="odd">
<td><a href="../element/input/datetime-local">datetime-local</a></td>
<td><code>yyyy-mm-ddThh:mm</code></td>
<td><code>&lt;input type="datetime-local" max="2019-12-25T23:59"&gt;</code></td>
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
**Note:** When the data entered by the user doesn\'t adhere to the
maximum value set, the value is considered invalid in constraint
validation and will match the
[`:invalid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:invalid)
and
[`:out-of-range`](https://developer.mozilla.org/en-US/docs/Web/CSS/:out-of-range)
pseudo-classes.
:::

See [Client-side validation](../constraint_validation) and
[`rangeOverflow`](https://developer.mozilla.org/en-US/docs/Web/API/ValidityState/rangeOverflow)
for more information.

For the [`<progress>`](../element/progress) element, the `max` attribute
describes how much work the task indicated by the `progress` element
requires. If present, must have a value greater than zero and be a valid
floating point number. For the [`<meter>`](../element/meter) element,
the `max` attribute defines the upper numeric bound of the measured
range. This must be greater than the minimum value ([`min`](min)
attribute), if specified. In both cases, if omitted, the value defaults
to 1.

<figure class="table-container">
<div class="_table">
<table class="no-markdown">
<caption>Syntax for <code>max</code> values for other elements</caption>
<thead>
<tr class="header">
<th>Input type</th>
<th>Syntax</th>
<th>Example</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="../element/progress"><code>&lt;progress&gt;</code></a></td>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/CSS/number">&lt;number&gt;</a></td>
<td><code>&lt;progress id="file" max="100" value="70"&gt; 70% &lt;/progress&gt;</code></td>
</tr>
<tr class="even">
<td><a href="../element/meter"><code>&lt;meter&gt;</code></a></td>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/CSS/number">&lt;number&gt;</a></td>
<td><code>&lt;meter id="fuel" min="0" max="100" low="33" high="66" optimum="80" value="40"&gt; at 40/100&lt;/meter&gt;</code></td>
</tr>
</tbody>
</table>

</figure>
:::

## Accessibility concerns {#accessibility_concerns}

::: section-content
Provide instructions to help users understand how to complete the form
and use individual form controls. Indicate any required and optional
input, data formats, and other relevant information. When using the
`max` attribute, ensure this maximum requirement is understood by the
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

  [HTML Standard\
  [\# attr-progress-max]{.small}](https://html.spec.whatwg.org/multipage/form-elements.html#attr-progress-max)
  --------------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
          Desktop                                                         Mobile                                                                                   
  ------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
          Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `max`   6         12     6         10                  11      6        4.4               18               6                     11              7               1.0
:::

::: _table
          Desktop                                                         Mobile                                                                                   
  ------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
          Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `max`   6         ≤18    16        No                  11      6        No                18               16                    11              10.3            1.0
:::

::: _table
          Desktop                                                         Mobile                                                                                   
  ------- --------- ------ --------- ------------------- ------- -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
          Chrome    Edge   Firefox   Internet Explorer   Opera   Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `max`   4         12     16        10                  ≤12.1   5        ≤37               18               16                    ≤12.1           4               1.0
:::

### html.elements.input.max

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

### html.elements.meter.max

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

### html.elements.progress.max

BCD tables only load in the browser with JavaScript enabled. Enable
JavaScript to view data.

## See also {#see_also}

::: section-content
-   [`step`](step)
-   [`min`](min)
-   other meter attributes:
    [`low`](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/low){.page-not-created},
    [`high`](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/high){.page-not-created},
    [`optimum`](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/optimum){.page-not-created}
-   [Constraint validation](../constraint_validation)
-   [Form
    validation](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation)
-   [`validityState.rangeOverflow`](https://developer.mozilla.org/en-US/docs/Web/API/ValidityState/rangeOverflow)
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
[https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/max](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/max){._attribution-link}
:::
