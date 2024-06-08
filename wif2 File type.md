# File Type
What method do we use to structure the data in the file.

# Type of file:
Needs to be a text based format. We do not need a binary format.
 - enables hand editing, readability, futureproofing.

### Possibilities
 - Yaml
   - most readable of the three. Best at configuration files.
      - uses indenting to define regions
   - a superset of json - it can contain json structures
   - a json schema is typically used to validate files
 - Json
   - Second most readable. Good at datafiles.
      - uses {} and indenting to define regions
   - a schema means we can verify correctness of a file.
      - https://json-schema.org/learn/getting-started-step-by-step
 - XML
   - least redable of the three.
      - relies on formatting symbols e.g. <>
   - a DTD or schema means we can verify correctness of a file.
   - very capable for complex descriptions (our needs are modest)

### Amazon web services have this to say:

#### When to use YAML vs. JSON

Thanks to pervasive support and integration with JavaScript, JSON is a more popular data serialization format for most use cases over YAML. JSON is used extensively in distributed software communications, web applications, configuration files, and APIs.

While YAML may appear to be a better choice based on data typing and its human-readable format, JSON is typically preferred for cross-compatibility. This is because many applications and services already parse JSON data format.

On the other hand, YAML has gained a strong presence in particular areas of computing because of its readability and support of comments. Notably, YAML is the primary data serialization format for configuration files in many automation, DevOps, and infrastructure as code (IaC) tools and services. For instance, YAML is often used in Docker and Kubernetes files.


## Examples:

#### YAML
```
---
# <- yaml supports comments, json does not
# did you know you can embed json in yaml?
# try uncommenting the next line
# { foo: 'bar' }

json:
  - rigid
  - better for data interchange
yaml:
  - slim and flexible
  - better for configuration
object:
  key: value
  array:
    - null_value: null
    - boolean: true
    - integer: 1
    - alias: aliases are like variables
    - alias: aliases are like variables
paragraph: |
  Blank lines denote
  paragraph breaks
content: |-
  Or we
  can auto
  convert line breaks
  to save space
alias:
  bar: baz
alias_reuse:
  bar: baz
```

#### JSON
```
{
  "json": [
    "rigid",
    "better for data interchange"
  ],
  "yaml": [
    "slim and flexible",
    "better for configuration"
  ],
  "object": {
    "key": "value",
    "array": [
      {
        "null_value": null
      },
      {
        "boolean": true
      },
      {
        "integer": 1
      },
      {
        "alias": "aliases are like variables"
      },
      {
        "alias": "aliases are like variables"
      }
    ]
  },
  "paragraph": "Blank lines denote\nparagraph breaks\n",
  "content": "Or we\ncan auto\nconvert line breaks\nto save space",
  "alias": {
    "bar": "baz"
  },
  "alias_reuse": {
    "bar": "baz"
  }
}
```

#### XML
```
<?xml version="1.0" encoding="UTF-8" ?>
 <root>
     <json>rigid</json>
     <json>better for data interchange</json>
     <yaml>slim and flexible</yaml>
     <yaml>better for configuration</yaml>
     <object>
         <key>value</key>
         <array>
             <null_value></null_value>
         </array>
         <array>
             <boolean>true</boolean>
         </array>
         <array>
             <integer>1</integer>
         </array>
         <array>
             <alias>aliases are like variables</alias>
         </array>
         <array>
             <alias>aliases are like variables</alias>
         </array>
     </object>
     <paragraph>
         Blank lines denote
         paragraph breaks
     </paragraph>
     <content>
         Or we
         can auto
         convert line breaks
     to save space</content>
     <alias>
         <bar>baz</bar>
     </alias>
     <alias_reuse>
         <bar>baz</bar>
     </alias_reuse>
 </root>
```