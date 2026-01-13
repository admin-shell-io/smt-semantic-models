# Semantic Models

This repository is for semantic models based on the [ESMF](https://eclipse-esmf.github.io/esmf-documentation/index.html) [Semantic Aspect Meta Model (SAMM)](https://eclipse-esmf.github.io/samm-specification) .

There are differnt ways how to create and use these Aspect Models in [Submodel Template Specifications](https://github.com/admin-shell-io/submodel-templates):

* They are used as master of the semantic definitions used in the so-called "Semantic Drived workflow" as desribed in [HOW TO CREATE A SUBMODEL TEMPLATE
SPECIFICATION](https://industrialdigitaltwin.org/en/wp-content/uploads/sites/2/2022/12/I40-IDTA-WS-Process-How-to-write-a-SMT-FINAL-.pdf)
* They are created on basis of an existing Submodel Template Specification
* They are build parallel to a Submodel Template Specification using a different workflow or using different semantic definitions as master
* They are build for reuse but no Submodel Template Specification is existing for these


[Best practices](https://eclipse-esmf.github.io/samm-specification/snapshot/appendix/best-practices.html) as defined in the SAMM specification should be followed.

The Aspect Models defined in this repository belong to the [namespaces](https://eclipse-esmf.github.io/samm-specification/snapshot/namespaces.html) starting with *io.admin-shell.idta*.

Models can reuse elements from different namespaces.

When defining and reusing elements from other aspect models, the following repositories with aspect models are allowed to be used besides the ones in this repository:

* [Catena-X aspect models](https://github.com/eclipse-tractusx/sldt-semantic-models), their namespaces start with *io.catenax*

There is a [command line tool in ESMF](https://eclipse-esmf.github.io/esmf-developer-guide/tooling-guide/samm-cli.html) that supports generation of different software artifacts like JSON schema, html etc.
In the "gen" Folder of the Aspect Models some of these software artifacts are contained.



