# Email Snippets :email:
A collection of snippets I use for HTML email development.

## Installation:

### Sublime Text 3

Clone or download this repo and copy the contents of `sublime-text` to `\Data\Packages\User\Snippets` in your [Sublime&nbsp;Text&nbsp;3](https://www.sublimetext.com/3) directory (find via *Preferences &rarr; Browse Packages* in menu).

### Visual Studio Code

Clone or download this repo and copy the contents of `visual-studio-code` to `\User\snippets` in your [Visual&nbsp;Studio&nbsp;Code](https://code.visualstudio.com) directory (find via *File &rarr; Preferences &rarr; User Snippets* in menu, usually `\AppData\Roaming\Code` on Windows).

## Usage:

Start with `em-qs`, then add `em-row` or `em-row-txt` for every horizontal section of the email design (name appropriately via the provided comments for organization). Stick to a **single-column** design with a narrow width for best results. If you really need things next to each other (i.e. columns), avoid `colspan` by nesting tables instead.

This approach results in a fixed-width layout everywhere media queries *aren't* supported, which ensures a reasonable result for **Gmail app** and **Outlook**. Use media queries to progressively enhance the experience where supported.

### Tips:

* Use tables for *everything* (no `<div>`, `<p>`, etc.)
* Only add negative space via padding on `<th>` elements (avoid margin)
* Most styles will go inline on `<th>` elements
* Avoid styles on `<tr>` elements
* Explicitly define **width** on `<table>` elements
* Explicitly define **width** and **height** on `<img>` elements

### Style:

To make your code easier to read and maintain, do this:

```html
<table align="left"
       border="0"
       cellpadding="0"
       cellspacing="0"
       width="600"
       style="border-collapse: collapse;
              border-spacing: 0;
              margin: 0;
              padding: 0;
              mso-table-lspace: 0;
              mso-table-rspace: 0;">
  <tr>
    <th align="left"
        valign="top"
        style="font-family: sans-serif, Roboto;
               font-size: 16px;
               font-weight: normal;
               mso-line-height-rule: exactly;
               line-height: 24px;
               padding: 0;
               word-wrap: break-word;">
      Lorem ipsum dolor sit amet...
    </th>
  </tr>
</table>
```

Not this:

```html
<table align="left" border="0" cellpadding="0" cellspacing="0" width="600" style="border-collapse: collapse; border-spacing: 0; margin: 0; padding: 0; mso-table-lspace: 0; mso-table-rspace: 0;">
  <tr>
    <th align="left" valign="top" style="font-family: sans-serif, Roboto; font-size: 16px; font-weight: normal; mso-line-height-rule: exactly; line-height: 24px; padding: 0; word-wrap: break-word;">
      Lorem ipsum dolor sit amet...
    </th>
  </tr>
</table>
```
You can always minify before sending :wink:
