## Classes, Attributes & Identifiers

Most markdown syntax above this section supports adding classes, attributes and identifiers
using [pandoc](https://pandoc.org/MANUAL.html) syntax without the need for a wrapper HTML element.

The syntax is `{.class-name attribute="value" attribute=value #id}`, which is placed at different locations depending
on the type of markdown.

<include src="codeAndOutput.md" boilerplate >
<variable name="highlightStyle">markdown</variable>
<variable name="code">
Apply classes, attributes, identifiers to block level markdown (eg. paragraphs, headings)
by leaving a space before '{' {.text-success #attribute-example}

#### heading {.text-info}

--- {.border-danger}

Apply the same to inline markdown (eg. bold text) by
omitting the **space**{.text-primary .bg-light header="attributes example"}
<!-- Use inspect element on the **space** word below to see the "header" attribute! -->
</variable>
</include>

Some other types of markdown have **different placements** of the curly group `{...}`. {.mb-4}

****Unordered and Ordered lists****

<include src="codeAndOutput.md" boilerplate >
<variable name="highlightStyle">markdown</variable>
<variable name="code" id="list-example">
* Apply to the list item itself like so {.text-success #list-item-id}
  * Curly groups after newlines apply to the closest nested list {.text-danger}
{.bg-light}
* Curly groups two lines after the last line apply to the top most list

{.alert-info}
</variable>
</include>

****Fenced code blocks****

Refer to the above [section](../formattingContents.html#line-numbering)!

<small>For a more detailed guide, see: https://www.npmjs.com/package/markdown-it-attrs</small>

<box type="warning" seamless>
Formatting features listed above this section support this syntax for attributes, classes and identifiers.
Those below this section do not.
</box>

<!-- Full syntax reference -->
<div id="short" class="d-none">

```
add a space before '{' for block level markdown {.class-name attribute="value" attribute=value #id}

don't add a space for **inline**{.text-danger} markdown
```
<small>For a more detailed guide, see: https://www.npmjs.com/package/markdown-it-attrs</small>
</div>

<!-- Reader facing features -->
<div id="examples" class="d-none">
<include src="attributes.md#list-example" />
</div>
