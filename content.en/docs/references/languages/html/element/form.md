

# \<form\>: The Form element



::: section-content
The `<form>` [HTML](../index) element represents a document section
containing interactive controls for submitting information.
:::

## Try it {#try_it}

::: section-content
::: iframe
::: {.output-header .border-rounded-top}
#### HTML Demo: \<form\> {#html-demo-form .output-heading}

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
    <form action="" method="get" class="form-example">
      <div class="form-example">
        <label for="name">Enter your name: </label>
        <input type="text" name="name" id="name" required />
      
      <div class="form-example">
        <label for="email">Enter your email: </label>
        <input type="email" name="email" id="email" required />
      
      <div class="form-example">
        <input type="submit" value="Subscribe!" />
      
    </form>
:::
:::

::: {#css-panel .section .hidden tabindex="0" role="tabpanel" aria-labelledby="css" aria-hidden="true"}
::: {#css-editor}
    form.form-example {
      display: table;
    }

    div.form-example {
      display: table-row;
    }

    label,
    input {
      display: table-cell;
      margin-bottom: 10px;
    }

    label {
      padding-right: 10px;
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

It is possible to use the
[`:valid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:valid) and
[`:invalid`](https://developer.mozilla.org/en-US/docs/Web/CSS/:invalid)
CSS
[pseudo-classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)
to style a `<form>` element based on whether the
[`elements`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLFormElement/elements)
inside the form are valid.
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes).

[`accept`](#accept) [Deprecated]{.visually-hidden}

:   Comma-separated [content
    types](https://developer.mozilla.org/en-US/docs/Web/SVG/Content_type)
    the server accepts.

    ::: {#sect1 .notecard .note}
    **Note:** **This attribute has been deprecated and should not be
    used.** Instead, use the [`accept`](input#accept) attribute on
    `<input type=file>` elements.
    :::

[`accept-charset`](#accept-charset)

:   Space-separated [character
    encodings](https://developer.mozilla.org/en-US/docs/Glossary/Character_encoding)
    the server accepts. The browser uses them in the order in which they
    are listed. The default value means [the same encoding as the
    page](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Encoding).
    (In previous versions of HTML, character encodings could also be
    delimited by commas.)

[`autocapitalize`](#autocapitalize) [Non-standard]{.visually-hidden}

:   A nonstandard attribute used by iOS Safari that controls how textual
    form elements should be automatically capitalized. `autocapitalize`
    attributes on a form elements override it on `<form>`. Possible
    values:

    -   `none`: No automatic capitalization.
    -   `sentences` (default): Capitalize the first letter of each
        sentence.
    -   `words`: Capitalize the first letter of each word.
    -   `characters`: Capitalize all characters --- that is, uppercase.

[`autocomplete`](#autocomplete)

:   Indicates whether input elements can by default have their values
    automatically completed by the browser. `autocomplete` attributes on
    form elements override it on `<form>`. Possible values:

    -   `off`: The browser may not automatically complete entries.
        (Browsers tend to ignore this for suspected login forms; see
        [The autocomplete attribute and login
        fields](https://developer.mozilla.org/en-US/docs/Web/Security/Securing_your_site/Turning_off_form_autocompletion#the_autocomplete_attribute_and_login_fields).)
    -   `on`: The browser may automatically complete entries.

[`name`](#name)

:   The name of the form. The value must not be the empty string, and
    must be unique among the `form` elements in the forms collection
    that it is in, if any.

[`rel`](#rel)

:   Controls the annotations and what kinds of links the form creates.
    Annotations include [`external`](../attributes/rel#external),
    [`nofollow`](../attributes/rel#nofollow),
    [`opener`](../attributes/rel#opener),
    [`noopener`](../attributes/rel#noopener), and
    [`noreferrer`](../attributes/rel#noreferrer). Link types include
    [`help`](../attributes/rel#help), [`prev`](../attributes/rel#prev),
    [`next`](../attributes/rel#next),
    [`search`](../attributes/rel#search), and
    [`license`](../attributes/rel#license). The
    [`rel`](../attributes/rel) value is a space-separated list of these
    enumerated values.
:::

### Attributes for form submission {#attributes_for_form_submission}

::: section-content
The following attributes control behavior during form submission.

[`action`](#action)

:   The URL that processes the form submission. This value can be
    overridden by a [`formaction`](button#formaction) attribute on a
    [`<button>`](button), [`<input type="submit">`](input/submit), or
    [`<input type="image">`](input/image) element. This attribute is
    ignored when `method="dialog"` is set.

[`enctype`](#enctype)

:   If the value of the `method` attribute is `post`, `enctype` is the
    [MIME
    type](https://en.wikipedia.org/wiki/Mime_type){target="_blank"} of
    the form submission. Possible values:

    -   `application/x-www-form-urlencoded`: The default value.
    -   `multipart/form-data`: Use this if the form contains
        [`<input>`](input) elements with `type=file`.
    -   `text/plain`: Useful for debugging purposes.

    This value can be overridden by [`formenctype`](button#formenctype)
    attributes on [`<button>`](button),
    [`<input type="submit">`](input/submit), or
    [`<input type="image">`](input/image) elements.

[`method`](#method)

:   The [HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP) method
    to submit the form with. The only allowed methods/values are (case
    insensitive):

    -   `post`: The
        [`POST`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/POST)
        method; form data sent as the [request
        body](https://developer.mozilla.org/en-US/docs/Web/API/Request/body).
    -   `get` (default): The
        [`GET`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/GET);
        form data appended to the `action` URL with a `?` separator. Use
        this method when the form [has no side
        effects](https://developer.mozilla.org/en-US/docs/Glossary/Idempotent).
    -   `dialog`: When the form is inside a [`<dialog>`](dialog), closes
        the dialog and causes a `submit` event to be fired on
        submission, without submitting data or clearing the form.

    This value is overridden by [`formmethod`](button#formmethod)
    attributes on [`<button>`](button),
    [`<input type="submit">`](input/submit), or
    [`<input type="image">`](input/image) elements.

[`novalidate`](#novalidate)

:   This Boolean attribute indicates that the form shouldn\'t be
    validated when submitted. If this attribute is not set (and
    therefore the form ***is*** validated), it can be overridden by a
    [`formnovalidate`](button#formnovalidate) attribute on a
    [`<button>`](button), [`<input type="submit">`](input/submit), or
    [`<input type="image">`](input/image) element belonging to the form.

[`target`](#target)

:   Indicates where to display the response after submitting the form.
    It is a name/keyword for a *browsing context* (for example, tab,
    window, or iframe). The following keywords have special meanings:

    -   `_self` (default): Load into the same browsing context as the
        current one.
    -   `_blank`: Load into a new unnamed browsing context. This
        provides the same behavior as setting [`rel="noopener"`](#rel)
        which does not set
        [`window.opener`](https://developer.mozilla.org/en-US/docs/Web/API/Window/opener).
    -   `_parent`: Load into the parent browsing context of the current
        one. If no parent, behaves the same as `_self`.
    -   `_top`: Load into the top-level browsing context (i.e., the
        browsing context that is an ancestor of the current one and has
        no parent). If no parent, behaves the same as `_self`.

    This value can be overridden by a [`formtarget`](button#formtarget)
    attribute on a [`<button>`](button),
    [`<input type="submit">`](input/submit), or
    [`<input type="image">`](input/image) element.
:::

## Examples

::: section-content
::: code-example
[html]{.language-name}

``` {signature="sgoC2PpCpEoHvF8uA7Pgbk3UfBmveJzLc6BlFK7Dqzo=" data-language="html"}
<!-- Form which will send a GET request to the current URL -->
<form method="get">
  <label>
    Name:
    <input name="submitted-name" autocomplete="name" />
  </label>
  <button>Save</button>
</form>

<!-- Form which will send a POST request to the current URL -->
<form method="post">
  <label>
    Name:
    <input name="submitted-name" autocomplete="name" />
  </label>
  <button>Save</button>
</form>

<!-- Form with fieldset, legend, and label -->
<form method="post">
  <fieldset>
    <legend>Do you agree to the terms?</legend>
    <label><input type="radio" name="radio" value="yes" /> Yes</label>
    <label><input type="radio" name="radio" value="no" /> No</label>
  </fieldset>
</form>
```
:::
:::

### Result

::: section-content
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
href="../content_categories#palpable_content">palpable content</a></td>
</tr>
<tr class="even">
<th scope="row">Permitted content</th>
<td><a href="../content_categories#flow_content">Flow content</a>, but
not containing <code>&lt;form&gt;</code> elements</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>None, both the starting and ending tag are mandatory.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>Any element that accepts <a
href="../content_categories#flow_content">flow content</a></td>
</tr>
<tr class="odd">
<th scope="row">Implicit ARIA role</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/form_role"><code>form</code></a></td>
</tr>
<tr class="even">
<th scope="row">Permitted ARIA roles</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/search_role"><code>search</code></a>,
<a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/none_role"><code>none</code></a>
or <a
href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/presentation_role"><code>presentation</code></a></td>
</tr>
<tr class="odd">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLFormElement"><code>HTMLFormElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: _table
  ------------------------------------------------------------------------------------------------
  Specification
  ------------------------------------------------------------------------------------------------
  [HTML Standard\
  [\#
  the-form-element]{.small}](https://html.spec.whatwg.org/multipage/forms.html#the-form-element)

  ------------------------------------------------------------------------------------------------
:::

## Browser compatibility {#browser_compatibility}

::: _table
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                     Desktop                                                                    Mobile                                                                      
  ------------------ ------------------ ------ --------- ---------- ------------------ -------- ------------------ ------------------ --------- ------------------ -------- ------------------
                     Chrome             Edge   Firefox   Internet   Opera              Safari   WebView Android    Chrome Android     Firefox   Opera Android      Safari   Samsung Internet
                                                         Explorer                                                                     for                          on IOS   
                                                                                                                                      Android                               

  `form`             1                  12     1         Yes        15                 ≤4       4.4                18                 4         14                 ≤3.2     1.0

  `accept`           1                  12     1         Yes        15                 3        4.4                18                 4         14                 2        1.0

  `accept-charset`   1                  12     1         Yes        15                 3        4.4                18                 4         14                 2        1.0

  `action`           1                  12     1         Yes        15                 ≤4       4.4                18                 4         14                 ≤3.2     1.0

  `autocapitalize`   43                 79     111       No         30                 No       43                 43                 111       30                 Yes      4.0

  `autocomplete`     14                 12     4         Yes        15                 6        4.4                18                 4         14                 6        1.0
                                                                                                                                                                            
                     The Google Chrome                              The Opera UI for            The Google Chrome  The Google Chrome            The Opera UI for            The Samsung
                     UI for                                         auto-complete               UI for             UI for                       auto-complete               Internet UI for
                     auto-complete                                  request varies,             auto-complete      auto-complete                request varies,             auto-complete
                     request varies,                                depending on                request varies,    request varies,              depending on                request varies,
                     depending on                                   whether                     depending on       depending on                 whether                     depending on
                     whether                                        `autocomplete` is           whether            whether                      `autocomplete` is           whether
                     `autocomplete` is                              set to `off` on             `autocomplete` is  `autocomplete` is            set to `off` on             `autocomplete` is
                     set to `off` on                                `<input>` elements          set to `off` on    set to `off` on              `<input>` elements          set to `off` on
                     `<input>` elements                             as well as their            `<input>` elements `<input>` elements           as well as their            `<input>` elements
                     as well as their                               form.                       as well as their   as well as their             form.                       as well as their
                     form.                                          Specifically, when          form.              form.                        Specifically, when          form.
                     Specifically, when                             a form has                  Specifically, when Specifically, when           a form has                  Specifically, when
                     a form has                                     `autocomplete` set          a form has         a form has                   `autocomplete` set          a form has
                     `autocomplete` set                             to `off` and its            `autocomplete` set `autocomplete` set           to `off` and its            `autocomplete` set
                     to `off` and its                               `<input>`                   to `off` and its   to `off` and its             `<input>`                   to `off` and its
                     `<input>`                                      element\'s                  `<input>`          `<input>`                    element\'s                  `<input>`
                     element\'s                                     `autocomplete`              element\'s         element\'s                   `autocomplete`              element\'s
                     `autocomplete`                                 attribute is not            `autocomplete`     `autocomplete`               attribute is not            `autocomplete`
                     attribute is not                               set, then if the            attribute is not   attribute is not             set, then if the            attribute is not
                     set, then if the                               user asks for               set, then if the   set, then if the             user asks for               set, then if the
                     user asks for                                  autofill                    user asks for      user asks for                autofill                    user asks for
                     autofill                                       suggestions for             autofill           autofill                     suggestions for             autofill
                     suggestions for                                the `<input>`               suggestions for    suggestions for              the `<input>`               suggestions for
                     the `<input>`                                  element, Opera              the `<input>`      the `<input>`                element, Opera              the `<input>`
                     element, Chrome                                might display a             element, Chrome    element, Chrome              might display a             element, Samsung
                     might display a                                message saying              might display a    might display a              message saying              Internet might
                     message saying                                 \'autocomplete has          message saying     message saying               \'autocomplete has          display a message
                     \'autocomplete has                             been disabled for           \'autocomplete has \'autocomplete has           been disabled for           saying
                     been disabled for                              this form.\' On             been disabled for  been disabled for            this form.\' On             \'autocomplete has
                     this form.\' On                                the other hand, if          this form.\' On    this form.\' On              the other hand, if          been disabled for
                     the other hand, if                             both the form and           the other hand, if the other hand, if           both the form and           this form.\' On
                     both the form and                              the input element           both the form and  both the form and            the input element           the other hand, if
                     the input element                              have                        the input element  the input element            have                        both the form and
                     have                                           `autocomplete` set          have               have                         `autocomplete` set          the input element
                     `autocomplete` set                             to `off`, the               `autocomplete` set `autocomplete` set           to `off`, the               have
                     to `off`, the                                  browser will not            to `off`, the      to `off`, the                browser will not            `autocomplete` set
                     browser will not                               display that                browser will not   browser will not             display that                to `off`, the
                     display that                                   message. For this           display that       display that                 message. For this           browser will not
                     message. For this                              reason, you should          message. For this  message. For this            reason, you should          display that
                     reason, you should                             set `autocomplete`          reason, you should reason, you should           set `autocomplete`          message. For this
                     set `autocomplete`                             to `off` for each           set `autocomplete` set `autocomplete`           to `off` for each           reason, you should
                     to `off` for each                              `<input>` that has          to `off` for each  to `off` for each            `<input>` that has          set `autocomplete`
                     `<input>` that has                             custom                      `<input>` that has `<input>` that has           custom                      to `off` for each
                     custom                                         auto-completion.            custom             custom                       auto-completion.            `<input>` that has
                     auto-completion.                                                           auto-completion.   auto-completion.                                         custom
                                                                                                                                                                            auto-completion.

  `enctype`          1                  12     1         Yes        15                 3        4.4                18                 4         14                 2        1.0

  `method`           1                  12     1         Yes        15                 3        4.4                18                 4         14                 2        1.0

  `name`             1                  12     1         Yes        15                 3        4.4                18                 4         14                 2        1.0

  `novalidate`       10                 12     4         10         15                 10.1     37                 18                 4         14                 10.3     1.0

  `rel`              108                108    111       No         94                 15.4     108                108                111       73                 15.4     21.0

  `target`           1                  12     1         Yes        15                 3        4.4                18                 4         14                 2        1.0
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   [HTML forms
    guide](https://developer.mozilla.org/en-US/docs/Learn/Forms)
-   Other elements that are used when creating forms:
    [`<button>`](button), [`<datalist>`](datalist),
    [`<fieldset>`](fieldset), [`<input>`](input), [`<label>`](label),
    [`<legend>`](legend), [`<meter>`](meter), [`<optgroup>`](optgroup),
    [`<option>`](option), [`<output>`](output),
    [`<progress>`](progress), [`<select>`](select),
    [`<textarea>`](textarea).
-   Getting a list of the elements in the form:
    [`HTMLFormElement.elements`](https://developer.mozilla.org/en-US/docs/Web/API/HTMLFormElement/elements)
-   [ARIA: Form
    role](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/form_role)
-   [ARIA: Search
    role](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles/search_role)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form){._attribution-link}
:::
