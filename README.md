<p align="center">
  <img  src="ydigital-logo.png" width="800" height="400" alt="y.digital logo">
</p>

# Conceptual Modeling and Linked Data Tools

- An opinionated list of practical tools for Conceptual Modeling and Linked Data.
- The list intends to present the most useful tools, rather than being comprehensive, _considering my team's development environment_.
- It focuses on free, open-source resources.
- The list provides a short review of the resource and brief considerations about its utility.


# Conceptual Modeling

Conceptual Modeling is the activity of formally describing aspects of the physical and social world around us for purposes of *understanding*, *communication*, and **problem-solving**. Humans, not machines, use conceptual models, although they can support computational tasks such as data model design, object-oriented programming, and automated reasoning. Therefore, the need for conceptual models is a human need to understand the environment through a form of intersubjective representation (often as diagrams).

Modeling the domain or the problem correctly is one of the most important tasks in a project, if not the most important, because grasping things incorrectly yields bad implementation and future interoperability issues.


- [**Tonto**](https://github.com/nemo-ufes/tonto)
  - Tonto is a textual ontology modeling language (a Domain-Specific Language, DSL). In a sense, it can be seen as a textual syntax for OntoUML. The project ships CLI tools, including syntax validation, automatic OWL generation complying with [gUFO](https://nemo-ufes.github.io/gufo/) (an OWL implementation of the Unified Foundational Ontology), instantiation of modeling patterns, and a VS Code extension. A complementary project includes a [visualizer](https://github.com/nemo-ufes/tonto-visualizer) for Tonto models. It is fully open-source.
  - The OntoUML language is implemented as a UML Class diagram profile, whose grammar is designed according to the [Unified Foundational Ontology](https://doi.org/10.3233/AO-210256) (to become an [ISO standard](https://www.iso.org/standard/89915.html) soon). Consequently, OntoUML models are constrained by useful upper ontological distinctions, which prevent certain modeling mistakes by design (for example, confusing entities of different natures, such as events, objects, propositions, and intrinsic properties), and provide modeling patterns (in contrast to isolated elements). In summary, the OntoUML language helps you create better conceptual models.
  - A detailed catalog of OntoUML models can be found [**here**](https://github.com/OntoUML/ontouml-models). The collection of models is meant to be comprehensive, *not qualitatively curated*, so they should be seen critically.

> [!WARNING]
> Tonto is replacing the OntoUML plugin for Visual Paradigm (described below). Therefore, Tonto is our first recommendation for OntoUML models.

- [**OntoUML plugin for Visual Paradigm**](https://github.com/OntoUML/ontouml-vp-plugin)
  - Visual Paradigm is a *professional* conceptual modeling tool suite. The [community edition](https://www.visual-paradigm.com/editions/community/) can be used for free for non-commercial purposes. It is the only _closed-source and paid tool_ (for commercial purposes) on this list. However, the entire [OntoUML ecosystem](https://github.com/OntoUML) (metamodel, schema, server, etc.) adopts open-source, permissive licenses, such as Apache 2.0. This means anyone is free to implement the OntoUML language in another tool or as a standalone tool. The plugin also includes several services available on the Tonto CLI, such as OntoUML syntax verification and OWL generation complying with gUFO.

> [!NOTE]
> In practice, you can create OntoUML diagrams using any tool that can create UML Class diagrams. However, Tonto and the OntoUML plugin for Visual Paradigm provide explicit support for this task, including automatic coloring of classes to denote their ontological nature, OWL generation, syntax verification, and others.

- [**Mermaid**](https://github.com/mermaid-js/mermaid)
  - Mermaid is an easy-to-use tool for diagram generation with a Markdown-like textual syntax, supporting flowcharts, various UML diagrams, the Entity-Relationship model, and many more. Since Mermaid has a textual syntax, Large Language Models can generate decent diagrams from prompts, which can be convenient for some use cases.
  - [PlantUML](https://github.com/plantuml/plantuml) is similar to Mermaid, but more powerful, although it is also more difficult to use.
  - [draw.io](https://github.com/jgraph/drawio) is a simple and nice diagramming tool, too simple for serious conceptual modeling, though.

- [**Archi**](https://github.com/archimatetool/archi)
  - Archi is a simple, cross-platform tool for [ArchiMate](https://en.wikipedia.org/wiki/ArchiMate), a standard Enterprise Architecture language, made by [The Open Group](https://www.opengroup.org/).

# Linked Data

By "Linked Data", we mean tools related to [Semantic Web standards](https://www.w3.org/2001/sw/wiki/Main_Page), particularly RDF, RDFS, OWL, SPARQL, and SHACL.

- [**Linked Data Patterns**](https://patterns.dataincubator.org/), a pattern catalogue for modelling, publishing, and consuming Linked Data.

- [**W3ID**](https://github.com/perma-id/w3id.org)
  - Free, secure, permanent URLs for Web applications. It is the best service of this kind. Having permanent URLs is crucial for Linked Data applications because they provide stable, unambiguous identifiers that allow data to be reliably connected, reused, and trusted over time.
  - The purl.archive is another example of this type of service; it is easier to use, but much less reliable, so it is not recommended. Services that generate [DOIs](https://www.doi.org/), such as Zenodo, have a different purpose and are not suitable for Linked Data applications.

- [**ReSpec**](https://github.com/speced/respec)
  - ReSpec is a JavaScript library that makes it easier to write technical documents. It was originally designed for the purpose of writing W3C specifications. The documentation of nearly all W3C standards follows the ReSpec template. Since most of it consists of HTML, ReSpec is easy to use, even if you do not know JavaScript.
  - There are tools, such as [pyLODE](https://github.com/RDFLib/pyLODE) and [Widoco](https://github.com/dgarijo/Widoco), that automatically generate documentation for an ontology. However, the resulting document only resembles a ReSpec document. [respecter](https://github.com/sdsc-ordes/respecter) is another tool, but it fully complies with the ReSpec template.

- [**The FAIR Cookbook**](https://github.com/FAIRplus/the-fair-cookbook)
  - Recipes to produce information artifacts that are **F**indable, **A**ccessible, **I**nteroperable, and **R**eusable.
  - The [FAIR principles](https://www.go-fair.org/fair-principles/) match perfectly with Linked Data both in research and industry contexts.

- [**RDFlib**](https://github.com/RDFLib)
  - The most mature Python library ecosystem for Linked Data.
  - Its JavaScript sibling is [rdflib.js](https://github.com/linkeddata/rdflib.js).
  - Alternatively, [**OpenRefine**](https://openrefine.org/) is a user-friendly GUI tool for working with messy data: cleaning, data transformation (supporting RDF), and other features.
  - For many similar libraries in other programming languages, see [Awesome Semantic Web: Programming](https://github.com/semantalytics/awesome-semantic-web?tab=readme-ov-file#programming).

- [**Jena toolkit**](https://jena.apache.org/documentation/)
  - The most comprehensive set of tools for RDF Linked Data (particularly, see [CLI tools](https://jena.apache.org/documentation/tools/)). It is much more performant than RDFLib. You can run it easily from the terminal instead of via multi-line scripts like the aforementioned libraries.

- [**Cool RDF**](https://github.com/cool-rdf/cool-rdf)
  - This is a set of high-level Java libraries and a CLI tool for working with RDF documents and OWL ontologies. One of its most useful features is its pretty-printed RDF/Turtle, which can normalize an RDF file to a certain degree. This guarantees that, under some conditions,  a given version of an RDF file is exactly (character by character) the same across users and applications, provided the file has the same content (the normalization sorts the triples, eliminates whitespace, and removes comments). This way, git version control works better for RDF. Yet, this does not substitute for true [canonicalization](https://www.w3.org/TR/rdf-canon/). But the purpose of canonicalization is not to handle (relatively small) ontologies for comparison (diff), but large datasets. I think Cool RDF still has a good use case in the ontology development process.

## Triplestores
  - [**Apache Jena Fuseki**](https://jena.apache.org/documentation/fuseki2/)
    - It is a solid triplestore developed by the [Apache Software Foundation](https://apache.org/).
    - This [**Jena Fuseki Server with Inference Support**](https://github.com/andybywire/jena-fuseki-inf) is a Docker image for running Fuseki with RDFS and OWL inference. It is the easiest way to run Fuseki.
    - [Docker image designed for RDF-related tasks in automated pipelines (ETL/ELT)](https://github.com/zazukoians/docker-node-java-jena/). It packages the Apache Jena stack, Node.js, and a comprehensive set of CLI tools for RDF processing, scripting, and reasoning.
  - [**Qlever**](https://github.com/ad-freiburg/qlever)
    - It is most likely the fastest triplestore available, developed by the [Algorithms and Data Structures Group](https://github.com/ad-freiburg) at the University of Freiburg. 
  - [**Oxigraph**](https://github.com/oxigraph/oxigraph)
    - It is less mature than the previous options, but it looks promising.

## Linked Data Editors
- [**Protégé**](https://protege.stanford.edu/)
  - It is a widely used ontology (OWL-focused) editor, though a bit buggy.
  - It can be used in combination with a text/code editor by reloading the Protégé session as needed.
  - Ultimately, text/code editors should always be used to write Linked Data specifications because they provide higher control and understanding.
 
- [**Neovim**](https://neovim.io/)
  - Hyperextensible Vim-based text editor. Modal, terminal-based text editors are the most powerful and resource-efficient, though they are not as easy to use as Visual Studio Code.
  - Check [this minimal Neovim config](https://codeberg.org/italojsoliveira/dotfiles) with basic syntax highlighting support for SPARQL, TTL, and Tonto.

## Ontologies and Vocabularies
> [!IMPORTANT]
> In my opinion, using some upper/foundational ontology is better than using none to build domain ontologies because upper ontologies provide essential modeling blocks that you, as a modeler, cannot avoid. Even if you do not explicitly adopt a specific upper ontology, your ontology design will implicitly assume upper ontological distinctions.
>
> Some may argue that certain projects do not need the complexity of a foundational ontology. I agree. However, these projects probably do not need to adopt Semantic Web standards either. Sometimes, a list of terms and definitions in CSV suffices.

  - [**gUFO**](https://nemo-ufes.github.io/gufo/)
    - gUFO (to become an [ISO standard](https://www.iso.org/standard/89915.html) soon) is a lightweight implementation of the Unified Foundational Ontology suitable for Semantic Web OWL 2 DL applications. gUFO is the most expressive upper ontology out there, made by computer science folks with philosophical knowledge. Besides the documentation, a good introduction is ["gUFO: A Gentle Foundational Ontology for Semantic Web Knowledge Graphs"](https://arxiv.org/abs/2603.20948). For more resources, check out the section RESOURCES (on the right-hand side of the page) of the Reddit [r/OntoUML_UFO_gUFO](https://www.reddit.com/r/OntoUML_UFO_gUFO/).
    - The [Basic Formal Ontology](https://github.com/BFO-ontology) (ISO/IEC 21838-2:2021) is another well-known upper ontology, widely used in the biomedical domain, although it is not as complete as gUFO.
  - [**PROV-O**](https://www.w3.org/TR/prov-o/)
    - It is a widely used provenance ontology, a W3C standard.
  - [**DCAT**](https://www.w3.org/TR/vocab-dcat-3/)
    - DCAT-3 is a W3C standard vocabulary for describing data catalogs and their contents on the Web.
  - [**DCMI Metadata Terms**](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/)
    - The Dublin Core Terms (ISO 15836-1:2017, IETF RFC 5013, ANSI/NISO Z39.85) are a widely used standard vocabulary to describe metadata of resources, such as documents, datasets, images, websites, or services.
  - [**SKOS**](https://www.w3.org/2004/02/skos/)
    - SKOS is a W3C standard for representing thesauri and taxonomies, which are much less complex than full-fledged domain ontologies.
    - For documentation and browsing, I recommend the following:
      - [SKOHUB](https://skohub.io/), simple and effective.
      - [SKOSMOS](https://skosmos.org/), more complicated, as it requires a PHP server and a triple store.

# Others

- [**Awesome Semantic Web**](https://github.com/semantalytics/awesome-semantic-web)
  - A miscellaneous list of resources related to Linked Data.
- [**RDF Playground**](https://rdfplayground.dcc.uchile.cl/)
  - For quick interaction with RDF data and SHACL shapes.
