# Anatomy Format

The plugin offers two formats for the Anatomy section: List beside artwork and Table below artwork.

![anatomy-format](https://github.com/EightShapes/specs-plugin/assets/1165904/4536b8d1-7aea-4e2a-9c04-44222c2fbbeb)

The *Anatomy format* feature is only available via the Pro subscription to the EightShapes Specs plugin.

* [What is included](#whatisincluded)
* [How it works](#howitworks)

## What is included <a id="whatisincluded"></a>

When an anatomy is generated, elements and their associated attributes are arranged in a vertical format by default. Alternatively, anatomy content may be displayed in tabular format, resulting in up to two tables for nested components and other detected elements.

## How it works <a id="howitworks"></a>

Refer to the [anatomy](../anatomy.md) for a description of how the anatomy is generated.

For the alternative tabular format displayed below the annotated artwork, the plugin will:

* Construct a "Nested components" table each nested component detected, with columns for component name (based on the nested layer name), dependency name, configured properties, and – when detected – associated linkes to dev resources
* Construct an "Elements with attributes" table, with columns for element name (based on layer name) and associated relevant attributes
* For instances, include the top layer in the "Other elements" table when that layer has relevant attributes

