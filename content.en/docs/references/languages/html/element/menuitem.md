

# \<menuitem\>



::: section-content
::: {#sect1 .notecard .deprecated}
**Deprecated:** This feature is no longer recommended. Though some
browsers might still support it, it may have already been removed from
the relevant web standards, may be in the process of being dropped, or
may only be kept for compatibility purposes. Avoid using it, and update
existing code if possible; see the [compatibility
table](#browser_compatibility) at the bottom of this page to guide your
decision. Be aware that this feature may cease to work at any time.
:::

::: {#sect2 .notecard .nonstandard}
**Non-standard:** This feature is non-standard and is not on a standards
track. Do not use it on production sites facing the Web: it will not
work for every user. There may also be large incompatibilities between
implementations and the behavior may change in the future.
:::

The `<menuitem>` [HTML](../index) element represents a command that a
user is able to invoke through a popup menu. This includes context
menus, as well as menus that might be attached to a menu button.

A command can either be defined explicitly, with a textual label and
optional icon to describe its appearance, or alternatively as an
*indirect command* whose behavior is defined by a separate element.
Commands can also optionally include a checkbox or be grouped to share
radio buttons. (Menu items for indirect commands gain checkboxes or
radio buttons when defined against elements `<input type="checkbox">`
and `<input type="radio">`.)
:::

## Attributes

::: section-content
This element includes the [global attributes](../global_attributes); in
particular `title` can be used to describe the command, or provide usage
hints.

[`checked`](#checked) [Deprecated]{.visually-hidden} [Non-standard]{.visually-hidden}

:   Boolean attribute which indicates whether the command is selected.
    May only be used when the `type` attribute is `checkbox` or `radio`.

[`command`](#command) [Deprecated]{.visually-hidden} [Non-standard]{.visually-hidden}

:   Specifies the ID of a separate element, indicating a command to be
    invoked indirectly. May not be used within a menu item that also
    includes the attributes `checked`, `disabled`, `icon`, `label`,
    `radiogroup` or `type`.

[`default`](#default) [Deprecated]{.visually-hidden} [Non-standard]{.visually-hidden}

:   This Boolean attribute indicates use of the same command as the
    menu\'s subject element (such as a `button` or `input`).

[`disabled`](#disabled) [Deprecated]{.visually-hidden} [Non-standard]{.visually-hidden}

:   Boolean attribute which indicates that the command is not available
    in the current state. Note that `disabled` is distinct from
    `hidden`; the `disabled` attribute is appropriate in any context
    where a change in circumstances might render the command relevant.

[`icon`](#icon) [Deprecated]{.visually-hidden} [Non-standard]{.visually-hidden}

:   Image URL, used to provide a picture to represent the command.

[`label`](#label)

:   The name of the command as shown to the user. Required when a
    `command` attribute is not present.

[`radiogroup`](#radiogroup) [Deprecated]{.visually-hidden} [Non-standard]{.visually-hidden}

:   This attribute specifies the name of a group of commands to be
    toggled as radio buttons when selected. May only be used where the
    `type` attribute is `radio`.

[`type`](#type) [Deprecated]{.visually-hidden} [Non-standard]{.visually-hidden}

:   This attribute indicates the kind of command, and can be one of
    three values.

    -   `command`: A regular command with an associated action. This is
        the missing value default.
    -   `checkbox`: Represents a command that can be toggled between two
        different states.
    -   `radio`: Represent one selection from a group of commands that
        can be toggled as radio buttons.
:::

## Examples

### HTML

::: section-content
::: code-example
[html]{.language-name}

``` {signature="BTiHTjP6sN+zysHcuCfxoMzzFEa1aUEgiVt8vdn3otY=" data-language="html"}
<!-- A  element with a context menu -->
<div contextmenu="popup-menu">Right-click to see the adjusted context menu

<menu type="context" id="popup-menu">
  <menuitem type="checkbox" checked>Checkbox</menuitem>
  <hr />
  <menuitem
    type="command"
    label="This command does nothing"
    icon="favicon-192x192.png">
    Commands don't render their contents.
  </menuitem>
  <menuitem
    type="command"
    label="This command has javascript"
    onclick="alert('command clicked')">
    Commands don't render their contents.
  </menuitem>
  <hr />
  <menuitem type="radio" radiogroup="group1">Radio Button 1</menuitem>
  <menuitem type="radio" radiogroup="group1">Radio Button 2</menuitem>
</menu>
```
:::
:::

### CSS

::: section-content
::: code-example
[css]{.language-name}

``` {signature="sZSFt7GZWQTjuNzkDA9M0lYCZVgpeqYK+GNWMLzPZQk=" data-language="css"}
div {
  width: 300px;
  height: 80px;
  background-color: lightgreen;
}
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
<td>None; it is a <a
href="https://developer.mozilla.org/en-US/docs/Glossary/Void_element">void
element</a>.</td>
</tr>
<tr class="odd">
<th scope="row">Tag omission</th>
<td>Must have a start tag and must not have an end tag.</td>
</tr>
<tr class="even">
<th scope="row">Permitted parents</th>
<td>The <a href="menu"><code>&lt;menu&gt;</code></a> element, where that
element is in the <em>popup menu</em> state. (If specified, the
<code>type</code> attribute of the <a
href="menu"><code>&lt;menu&gt;</code></a> element must be
<code>popup</code>; if missing, the parent element of the <a
href="menu"><code>&lt;menu&gt;</code></a> must itself be a <a
href="menu"><code>&lt;menu&gt;</code></a> in the <em>popup menu</em>
state.)</td>
</tr>
<tr class="odd">
<th scope="row">Permitted ARIA roles</th>
<td>None</td>
</tr>
<tr class="even">
<th scope="row">DOM interface</th>
<td><a
href="https://developer.mozilla.org/en-US/docs/Web/API/HTMLMenuItemElement"><code>HTMLMenuItemElement</code></a></td>
</tr>
</tbody>
</table>

</figure>
:::

## Specifications

::: section-content
Not part of any current specifications.
:::

## Browser compatibility {#browser_compatibility}

## See also {#see_also}

::: section-content
-   [HTML context menus in Firefox (Screencast and
    Code)](https://hacks.mozilla.org/2011/11/html5-context-menus-in-firefox-screencast-and-code/){target="_blank"}
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/menuitem](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/menuitem){._attribution-link}
:::
