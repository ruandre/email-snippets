# Email Snippets
A collection of snippets I use for HTML email development.

## Installation

### Sublime Text 3

Clone or download this repository and copy the contents of the `sublime-text` folder to `\Data\Packages\User\Snippets` in your [Sublime Text 3](https://www.sublimetext.com/3) directory (find via *Preferences &rarr; Browse Packages* in menu).

## Usage

Start with `em-qs`, then add `em-row` or `em-row-txt` for every horizontal section of the email design (name appropriately via the provided comments for organization). Try to keep to a single-column design with a fairly narrow width for best results. If you really need things next to each other (i.e. columns), avoid `colspan` by nesting tables instead.

### Tips:

* **When in doubt, nest deeper**
* Only add negative space via padding on `<th>` elements (no margin)
* Most styles will go inline on `<th>` elements; use these for *everything* including text (no `<p>`)
* Avoid styles on `<tr>` elements
* Explicitly define **width** on `<table>` elements
* Explicitly define **width** and **height** on `<img>` elements
