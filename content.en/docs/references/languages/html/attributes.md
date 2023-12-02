

# HTML attribute reference



::: section-content
Elements in HTML have **attributes**; these are additional values that
configure the elements or adjust their behavior in various ways to meet
the criteria the users want.
:::

## Attribute list {#attribute_list}

::: section-content
:::

## Content versus IDL attributes {#content_versus_idl_attributes}

::: section-content
In HTML, most attributes have two faces: the **content attribute** and
the **IDL (Interface Definition Language) attribute**.

The content attribute is the attribute as you set it from the content
(the HTML code) and you can set it or get it via
[`element.setAttribute()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/setAttribute)
or
[`element.getAttribute()`](https://developer.mozilla.org/en-US/docs/Web/API/Element/getAttribute).
The content attribute is always a string even when the expected value
should be an integer. For example, to set an [`<input>`](element/input)
element\'s `maxlength` to 42 using the content attribute, you have to
call `setAttribute("maxlength", "42")` on that element.

The IDL attribute is also known as a JavaScript property. These are the
attributes you can read or set using JavaScript properties like
`element.foo`. The IDL attribute is always going to use (but might
transform) the underlying content attribute to return a value when you
get it and is going to save something in the content attribute when you
set it. In other words, the IDL attributes, in essence, reflect the
content attributes.

Most of the time, IDL attributes will return their values as they are
really used. For example, the default `type` for
[`<input>`](element/input) elements is \"text\", so if you set
`input.type="foobar"`, the `<input>` element will be of type text (in
the appearance and the behavior) but the \"type\" content attribute\'s
value will be \"foobar\". However, the `type` IDL attribute will return
the string \"text\".

IDL attributes are not always strings; for example, `input.maxlength` is
a number (a signed long). When using IDL attributes, you read or set
values of the desired type, so `input.maxlength` is always going to
return a number and when you set `input.maxlength`, it wants a number.
If you pass another type, it is automatically converted to a number as
specified by the standard JavaScript rules for type conversion.

IDL attributes can [reflect other
types](https://html.spec.whatwg.org/multipage/urls-and-fetching.html){target="_blank"}
such as unsigned long, URLs, booleans, etc. Unfortunately, there are no
clear rules and the way IDL attributes behave in conjunction with their
corresponding content attributes depends on the attribute. Most of the
time, it will follow [the rules laid out in the
specification](https://html.spec.whatwg.org/multipage/urls-and-fetching.html){target="_blank"},
but sometimes it doesn\'t. HTML specifications try to make this as
developer-friendly as possible, but for various reasons (mostly
historical), some attributes behave oddly (`select.size`, for example)
and you should read the specifications to understand how exactly they
behave.
:::

## Boolean Attributes {#boolean_attributes}

::: section-content
Some content attributes (e.g. `required`, `readonly`, `disabled`) are
called [boolean
attributes](https://html.spec.whatwg.org/multipage/common-microsyntaxes.html#boolean-attributes){target="_blank"}.
If a boolean attribute is present, its value is **true**, and if it\'s
absent, its value is **false**.

HTML defines restrictions on the allowed values of boolean attributes:
If the attribute is present, its value must either be the empty string
(equivalently, the attribute may have an unassigned value), or a value
that is an ASCII case-insensitive match for the attribute\'s canonical
name, with no leading or trailing whitespace. The following examples are
valid ways to mark up a boolean attribute:

::: code-example
[html]{.language-name}

``` {signature="FImXsvfGpKqJeugjzmuddTJbODk1lrVwugy/bosFT2U=" data-language="html"}
<div itemscope>This is valid HTML but invalid XML.
<div itemscope=itemscope>This is also valid HTML but invalid XML.
<div itemscope="">This is valid HTML and also valid XML.
<div itemscope="itemscope">
  This is also valid HTML and XML, but perhaps a bit verbose.

```
:::

To be clear, the values \"`true`\" and \"`false`\" are not allowed on
boolean attributes. To represent a false value, the attribute has to be
omitted altogether. This restriction clears up some common
misunderstandings: With `checked="false"` for example, the element\'s
`checked` attribute would be interpreted as **true** because the
attribute is present.
:::

## Event handler attributes {#event_handler_attributes}

::: section-content
::: {#sect8 .notecard .warning}
**Warning:** The use of event handler content attributes is discouraged.
The mix of HTML and JavaScript often produces unmaintainable code, and
the execution of event handler attributes may also be blocked by content
security policies.
:::

In addition to the attributes listed in the table above, global [event
handlers](https://developer.mozilla.org/en-US/docs/Web/Events/Event_handlers#using_onevent_properties)
--- such as
[`onclick`](https://developer.mozilla.org/en-US/docs/Web/API/Element/click_event)
--- can also be specified as [content
attributes](#content_versus_idl_attributes) on all elements.

All event handler attributes accept a string. The string will be used to
synthesize a [JavaScript
function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions)
like `function name(/*args*/) {body}`, where `name` is the attribute\'s
name, and `body` is the attribute\'s value. The handler receives the
same parameters as its JavaScript event handler counterpart --- most
handlers receive only one `event` parameter, while `onerror` receives
five: `event`, `source`, `lineno`, `colno`, `error`. This means you can,
in general, use the `event` variable within the attribute.

::: code-example
[html]{.language-name}

``` {signature="KFAtHH+PHZfVp5Ktp2hjuCvcYbRYlWGQ3+ibriG4fxA=" data-language="html"}
<div onclick="console.log(event)">Click me!
<!-- The synthesized handler has a name; you can reference itself -->
<div onclick="console.log(onclick)">Click me!
```
:::
:::

## See also {#see_also}

::: section-content
-   [HTML elements](element)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes){._attribution-link}
:::
