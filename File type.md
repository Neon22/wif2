# File Type
What method do we use to structure the data in the file.

# Type of file:
Needs to be a text based format. We do not need a binary format.
 - enables hand editing, readability, futureproofing.

#### Possibilities
 - Yaml
   - most readable of the three. Best at configuration files.
   - a superset of json - it can contain json structures
 - Json
   - Second most readable. Good at datafiles.
      - uses {} and indenting to define regions
   - a schema means we can verify correctness of a file.
      - https://json-schema.org/learn/getting-started-step-by-step
 - XML
   - least redable of the three.
      - relies on formatting symbols e.g. <>
   - a schema means we can verify correctness of a file.
   - very capable for complex descriptions (our needs are modest)

Amaon web services have this to say:
When to use YAML vs. JSON
Thanks to pervasive support and integration with JavaScript, JSON is a more popular data serialization format for most use cases over YAML. JSON is used extensively in distributed software communications, web applications, configuration files, and APIs.

While YAML may appear to be a better choice based on data typing and its human-readable format, JSON is typically preferred for cross-compatibility. This is because many applications and services already parse JSON data format.

On the other hand, YAML has gained a strong presence in particular areas of computing because of its readability and support of comments. Notably, YAML is the primary data serialization format for configuration files in many automation, DevOps, and infrastructure as code (IaC) tools and services. For instance, YAML is often used in Docker and Kubernetes files.
