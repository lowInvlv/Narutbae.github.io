

# \<time\>: The (Date) Time element



::: section-content
The `<time>` [HTML](../index) element represents a specific period in
time. It may include the `datetime` attribute to translate dates into
machine-readable format, allowing for better search engine results or
custom features such as reminders.

It may represent one of the following:

-   A time on a 24-hour clock.
-   A precise date in the [Gregorian
    calendar](https://en.wikipedia.org/wiki/Gregorian_calendar){target="_blank"}
    (with optional time and timezone information).
-   [A valid time
    duration](https://html.spec.whatwg.org/multipage/common-microsyntaxes.html#valid-duration-string){target="_blank"}.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<time\> {#html-demo-time .output-heading}

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
    <p>
      The Cure will be celebrating their 40th anniversary on <time datetime="2018-07-07">July 7</time> in London's Hyde
      Park.
    </p>

    <p>
      The concert starts at <time datetime="20:00">20:00</time> and you'll be able to enjoy the band for at least
      <time datetime="PT2H30M">2h 30m</time>.
    </p>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    time {
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
Like all other HTML elements, this element supports the [global
attributes](../global_attributes).

[`datetime`](#datetime)

:   This attribute indicates the time and/or date of the element and
    must be in one of the formats described below.
:::

## Usage notes {#usage_notes}

::: section-content
This element is for presenting dates and times in a machine-readable
format. For example, this can help a user agent offer to add an event to
a user\'s calendar.

This element should not be used for dates prior to the introduction of
the Gregorian calendar (due to complications in calculating those
dates).

The *datetime value* (the machine-readable value of the datetime) is the
value of the element\'s `datetime` attribute, which must be in the
proper format (see below). If the element does not have a `datetime`
attribute, **it must not have any element descendants**, and the
*datetime value* is the element\'s child text content.
:::

### Valid datetime values {#valid_datetime_values}

::: section-content

[a valid year string](#a_valid_year_string)

:   `2011`

[a valid month string](#a_valid_month_string)

:   `2011-11`

[a valid date string](#a_valid_date_string)

:   `2011-11-18`

[a valid yearless date string](#a_valid_yearless_date_string)

:   `11-18`

[a valid week string](#a_valid_week_string)

:   `2011-W47`

[a valid time string](#a_valid_time_string)

:   `14:54`

    `14:54:39`

    `14:54:39.929`

[a valid local date and time string](#a_valid_local_date_and_time_string)

:   `2011-11-18T14:54:39.929`

    `2011-11-18 14:54:39.929`

[a valid global date and time string](#a_valid_global_date_and_time_string)

:   `2011-11-18T14:54:39.929Z`

    `2011-11-18T14:54:39.929-0400`

    `2011-11-18T14:54:39.929-04:00`

    `2011-11-18 14:54:39.929Z`

    `2011-11-18 14:54:39.929-0400`

    `2011-11-18 14:54:39.929-04:00`

[a valid duration string](#a_valid_duration_string)

:   `PT4H18M3S`
:::

## Examples

### Simple example {#simple_example}

::: section-content
#### HTML

::: code-example
[html]{.language-name}

``` {signature="9A96bUiO8BFgtvVlGZYBr+e/tr6MRVBzNdiSOEW5d50=" data-language="html"}
<p>The concert starts at <time datetime="2018-07-07T20:00:00">20:00</time>.</p>
```
:::

#### Result

::: {#sect1 .code-example}
::: iframe
:::
:::
:::

### `datetime` example {#datetime_example}

::: section-content
#### HTML {#html_2}

::: code-example
[html]{.language-name}

``` {signature="QmL9RorcB8np3iKDnCUh89LHS2dfPF/ns89Y50Le1GE=" data-language="html"}
<p>
  The concert took place on <time datetime="2001-05-15T19:00">May 15</time>.
</p>
```
:::

#### Result {#result_2}

::: {#sect2 .code-example}
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
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/structural_roles#structural_roles_with_html_equivalents"><code>time</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td>Any</td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLTimeElement"><code>HTMLTimeElement</code></a></td>
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
  the-time-element]{.small}](https://html.spec.whatwg.org/multipage/text-level-semantics.html#the-time-element)

  ---------------------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
               Desktop                                                              Mobile                                                                                   
  ------------ --------- ------ --------- ------------------- ------------ -------- ----------------- ---------------- --------------------- --------------- --------------- ------------------
               Chrome    Edge   Firefox   Internet Explorer   Opera        Safari   WebView Android   Chrome Android   Firefox for Android   Opera Android   Safari on IOS   Samsung Internet
  `time`       62        ≤18    22        No                  4911.5--12   7        62                62               22                    4611.5--12      4               8.0
  `datetime`   62        ≤18    22        No                  4911.5--12   7        62                62               22                    4611.5--12      4               8.0
:::

## See also {#see_also}

::: section-content
-   The [`<data>`](data) element, allowing to signal other kind of
    values.
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/time](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/time){._attribution-link}
:::
