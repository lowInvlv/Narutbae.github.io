

# contextmenu



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

The `contextmenu` [global attribute](../global_attributes) is the
[**id**](id) of a [`<menu>`](../element/menu) to use as the contextual
menu for this element.

A *context menu* is a menu that appears upon user interaction, such as a
right-click. HTML now allows us to customize this menu. Here are some
implementation examples, including nested menus.
:::

## Example

### HTML

::: section-content
::: code-example
[html]{.language-name}

``` {signature="QhNyPy22A0r9KkMfsZ0fR00iPiQhCuOV6HckH/8HFw0=" data-language="html"}
<body contextmenu="share">
  <menu type="context" id="share">
    <menu label="share">
      <menuitem label="Twitter" onclick="shareViaTwitter()"></menuitem>
      <menuitem label="Facebook" onclick="shareViaFacebook()"></menuitem>
    </menu>
  </menu>
  <ol>
    <li>
      Anywhere in the example you can share the page on Twitter and Facebook
      using the Share menu from your context menu.
    </li>
    <li contextmenu="changeFont" id="fontSizing">
      On this specific list element, you can change the size of the text by
      using the "Increase/Decrease font" actions from your context menu
    </li>
    <menu type="context" id="changeFont">
      <menuitem label="Increase Font" onclick="incFont()"></menuitem>
      <menuitem label="Decrease Font" onclick="decFont()"></menuitem>
    </menu>
    <li contextmenu="ChangeImage" id="changeImage">
      On the image below, you can fire the "Change Image" action in your Context
      Menu.<br />
      <img
        src="promobutton_mdn5.png"
        contextmenu="ChangeImage"
        id="promoButton"
        alt="Better CSS Docs for a better web" />
      <menu type="context" id="ChangeImage">
        <menuitem label="Change Image" onclick="changeImage()"></menuitem>
      </menu>
    </li>
  </ol>
</body>
```
:::
:::

### JavaScript

::: section-content
::: code-example
[js]{.language-name}

``` {signature="QhqRoqG+VaPDfOF0ZkIvRNC5ZcHciTll9eKqKjxf3xY=" data-language="js"}
function shareViaTwitter() {
  window.open(
    "https://twitter.com/intent/tweet?text=" +
      "Hurray! I am learning ContextMenu from MDN via Mozilla",
  );
}

function shareViaFacebook() {
  window.open(
    "https://facebook.com/sharer/sharer.php?u=" +
      "https://developer.mozilla.org/en/HTML/Element/Using_HTML_context_menus",
  );
}

function incFont() {
  document.getElementById("fontSizing").style.fontSize = "larger";
}

function decFont() {
  document.getElementById("fontSizing").style.fontSize = "smaller";
}

function changeImage() {
  const index = Math.ceil(Math.random() * 39 + 1);
  document.images[0].src = `${index}.png`;
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

## Specifications

::: section-content
The [contextmenu attribute is
obsolete](https://html.spec.whatwg.org/multipage/obsolete.html#attr-contextmenu){target="_blank"}
and will be removed from all browsers.
:::

## Browser compatibility {#browser_compatibility}

::: _table
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------
                  Desktop                                                Mobile                                                                         
  --------------- --------- ------ --------- ---------- ------- -------- --------- --------- --------------------------------------- --------- -------- ----------
                  Chrome    Edge   Firefox   Internet   Opera   Safari   WebView   Chrome    Firefox for Android                     Opera     Safari   Samsung
                                             Explorer                    Android   Android                                           Android   on IOS   Internet

  `contextmenu`   No        No     9--85     No         No      No       No        No        32--56                                  No        No       No
                                                                                                                                                        
                                                                                             Support for the `contextmenu` attribute                    
                                                                                             has been removed from Firefox for                          
                                                                                             Android (See [bug                                          
                                                                                             1424252](https://bugzil.la/1424252)).                      
  ----------------------------------------------------------------------------------------------------------------------------------------------------------------
:::

## See also {#see_also}

::: section-content
-   All [global attributes](../global_attributes)
:::

::: _attribution
© 2005--2023 MDN contributors.\
Licensed under the Creative Commons Attribution-ShareAlike License v2.5
or later.\
[https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/contextmenu](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/contextmenu){._attribution-link}
:::
