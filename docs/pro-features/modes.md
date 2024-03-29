# Modes

The plugin can produce a Modes section that includes specs and artwork of items with layer-bound variables that (a) have multiple modes with (b) values that differ by mode.

![image](https://github.com/EightShapes/specs-plugin/assets/1165904/0c7e6e23-14f7-44c9-80b7-3ec4d2bb6083)

The *Figma variables formatting* feature is only available via the Pro subscription to the EightShapes Specs plugin.

* [What is included](#whatisincluded)
* [How it works](#howitworks)
* [Examples](#examples)
* [FAQs](#faqs)

## What is included <a id="whatisincluded"></a>

A Modes section is added to the item's spec if one or more variables with values that vary over two or more modes. A section is added for each matched variable collection, with an exhibit of artwork and attribute specs for each mode's varying attributes.

## How it works <a id="howitworks"></a>

If a user selects to include a Modes section, the plugin will:
– traverse all the item's layers to find variables bound to each layer
- evaluate the variables to determine if it's relevant (it vary across two or more modes)
- create a Modes specs subsection for each variable collection with a relevant variable

In each subsection corresponding to a variable collection, the plugin will:
- show the item with that mode applied
- compare the item's relevant variables across modes
- include attribute-by-attribute specs of how variable values change

## Examples <a id="examples"></a>

![image](https://github.com/EightShapes/specs-plugin/assets/1165904/e6aae829-98eb-434f-892a-5084142c2a90)

Here, the Color variable collection varies colors across two modes: light and dark. With those variables applied to text and alert colors, the `Alert` component will result in a two moded display showing both light and dark modes and the values corresponding to each relevant variable.

Note that `Icon` and `Button` specs are not included; instead, _also_ create specs for each nested component separately.

## FAQs <a id="faqs"></a>

#### Will the Modes section include subsections when a variable from a variable collection with one mode are detected?

No. The Modes section will only include a subsection for a variable collection when that collection has two or more modes.

#### Will the Modes section add spec'ed attributes for variables that don't vary across modes?

No. Instead, such variables would be depicted in the Anatomy section or – should such a variable be changed across Property-based alternatives – in the Props section.

#### Will the Modes section overlay spacing annotations for attributes like padding and item spacing, like the Layout and Spacing section does?

No, not at this time. Such overlays are placed _layer-by-layer_ in the Layout and Spacing section. In the Modes section, artwork is presented for the overall item, such that layout and spacing annotations would be _for all layers combined_, muddling the display. Further work may follow to consider overlaying such annotation in a visually clear way.
