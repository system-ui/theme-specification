
# RFC: Theme Specification: Level 2

The current specification is intentionally limited in scope to allow for extension and interpretation for how typography, color, layout and other values are grouped and defined.
This allows for some level of interoperability among the different libraries that adhere to the spec, but does not ensure interoperability of the theme objects themselves.

This proposal is for an optional specification that defines a schema for some of the individual scales in a theme object.
This is intended to make themes swappable and allow for transformations for use in libraries that do not adhere to this exact specification.

For the purposes of this document, the term *level 1* is used to reference the current theme specification as-is,
and the term *level 2* is this optional specification that builds on top of the current specification's foundation.

## Schema

While the overall object is still intended to be extensible, the following keys should be defined in a theme that conforms to level 2.

```
{
  colors: {
    text: String,
    background: String,
    primary: String,
    secondary: String,
    accent: String,
    muted: String,
  },
  fonts: {
    body: String,
    heading: String,
    monospace: String,
  },
  fontWeights: {
    body: String or Number,
    heading: String or Number,
    bold: String or Number,
  },
  lineHeights: {
    body: String or Number,
    heading: String or Number,
  },
  fontSizes: Array (length 10),
  space: Array (length 10),
}
```

