# Conceptual Modeling and Linked Data Tools

- An opinionated list of practical tools for Conceptual Modeling and Linked Data.
- The list intends to present the most useful tools, instead of being comprehensive, _considering my team's development environment_.
- It focuses on free, open-source resources.
- The list provides a short review of the resource and brief considerations about its utility.


# Conceptual Modeling

Conceptual Modeling is the activity of formally describing some aspects of the physical and social world around us for purposes of *understanding* and *communication*. Conceptual models are intended to be used by humans, not machines, although they can support computational tasks, such as data model design and automated reasoning. The need for conceptual models is, therefore, a human need to understand the environment by a form of intersubjective representation (very often a diagrammatic form).

Modeling the domain or the problem correctly is one of the most important tasks in a project, if not the most important one, because grasping things incorrectly yields bad implementation and future interoperability issues.

- [**OntoUML plugin for Visual Paradigm**](https://github.com/OntoUML/ontouml-vp-plugin)
  - Visual Paradigm is a *professional* conceptual modeling tool suite. The [community edition](https://www.visual-paradigm.com/editions/community/) can be used for free for non-commercial purposes. It is the only closed-source and paid tool (for commercial purposes) on this list. However, the entire [OntoUML ecosystem](https://github.com/OntoUML) (metamodel, schema, server, etc.) adopts open-source, permissive licenses, such as Apache 2.0. This means anyone is free to implement the OntoUML language in another tool or as a standalone tool.
  - The OntoUML is implemented as a UML Class diagram profile, whose grammar is designed according to the [Unified Foundational Ontology](https://doi.org/10.3233/AO-210256) (to become an [ISO standard](https://www.iso.org/standard/89915.html) soon). Consequently, the OntoUML models are constrained by useful upper ontological distinctions, which prevent certain modeling mistakes by design (for example, confusing entities of different natures, such as events, objects, propositions, and intrinsic properties), and provide modeling patterns (in contrast to isolated elements). In summary, OntoUML language helps you create better conceptual models. 
  - The OntoUML plugin includes several services, such as syntax verification and OWL generation (complying with [gUFO](https://nemo-ufes.github.io/gufo/), an OWL implementation of the Unified Foundational Ontology). This way, it is possible to build a conceptual model and generate its Linked Data implementation automatically, guaranteeing a higher level of quality thanks to OntoUML's constraints.
  - A detailed catalog of OntoUML models can be found [**here**](https://github.com/OntoUML/ontouml-models). The collection of models is meant to be comprehensive, *not qualitatively curated*, so they should be seen critically.

> [!NOTE]
> In practice, you can create OntoUML models using any tool that can create UML Class diagrams. However, the OntoUML plugin for Visual Paradigm offers explicit support for this task, including automatic coloring classes to denote their ontological nature, OWL generation, syntax verification, and others.

- [**Mermaid**](https://github.com/mermaid-js/mermaid)
  - Mermaid is an easy-to-use tool for diagram generation with a Markdown-like textual syntax, supporting flow charts, various UML diagrams, Entity-Relationship model, and many more. Since Mermaid has a textual syntax, Large Language Models can generate decent diagrams from prompts, which can be convenient for some use cases.
  - [PlantUML](https://github.com/plantuml/plantuml) is similar to Mermaid, but more powerful, although it is also more difficult to use.
  - [draw.io](https://github.com/jgraph/drawio) is a simple and nice diagramming tool, too simple for serious conceptual modeling, though.

- [**Archi**](https://github.com/archimatetool/archi)
  - Archi is a simple, cross-platform tool for [ArchiMate](https://en.wikipedia.org/wiki/ArchiMate), a standard Enterprise Architecture language, made by [The Open Group](https://www.opengroup.org/).

# Linked Data

By "Linked Data", we mean tools related to [Semantic Web standards](https://www.w3.org/2001/sw/wiki/Main_Page), particularly RDF, RDFS, OWL, SPARQL, and SHACL.

- [**W3ID**](https://github.com/perma-id/w3id.org)
  - Free, secure, permanent URLs for Web applications. It is the best service of this kind. Having permament URLs is crucial for Linked Data applications because they provide stable, unambiguous identifiers that allow data to be reliably connected, reused, and trusted over time.
  - The purl.archive is another example of this type of service; it is easier to use, but much less reliable, so it is not recommended. Services that generate [DOIs](https://www.doi.org/), such as Zenodo, have a different purpose, not suitable for Linked Data applications.

- [**ReSpec**](https://github.com/speced/respec)
  - ReSpec is a JavaScript library that makes it easier to write technical documents. It was originally designed for the purpose of writing W3C specifications. The documentation of nearly all W3C standards follows the ReSpec template. Since most of it consists of HTML, ReSpec is easy to use, even if you do not know JavaScript.
  - There are tools, such as [pyLODE](https://github.com/RDFLib/pyLODE) and [Widoco](https://github.com/dgarijo/Widoco), that automatically generate documentation for an ontology. However, the resulting document only resembles a ReSpec document. My recommendation is to use these tools just to generate HTML snippets that will be added to the ReSpec template.

- [**The FAIR Cookbook**](https://github.com/FAIRplus/the-fair-cookbook)
  - Recipes to produce information artifacts that are **F**indable, **A**ccessible, **I**nteroperable, and **R**eusable.
  - The [FAIR principles](https://www.go-fair.org/fair-principles/) match perfectly with Linked Data both in research and industry contexts.

- [**RDFlib**](https://github.com/RDFLib)
  - The best Python library and ecosystem for Linked Data.
  - Its JavaScript sibling is [rdflib.js](https://github.com/linkeddata/rdflib.js).

- **Triplestores**
  - [**Apache Jena Fuseki**](https://jena.apache.org/documentation/fuseki2/)
    - It is a solid triplestore developed by the [Apache Software Foundation](https://apache.org/).
    - This [**Jena Fuseki Server with Inference Support**](https://github.com/andybywire/jena-fuseki-inf) is a Docker image for running Fuseki with RDFS and OWL inference. It is the easiest way to run Fuseki.
  - [**Qlever**](https://github.com/ad-freiburg/qlever)
    - It is most likely the fastest triplestore available, developed by the [Algorithms and Data Structures Group](https://github.com/ad-freiburg) at the University of Freiburg. 
  - [**Oxigraph**](https://github.com/oxigraph/oxigraph)
    - It is less mature than the previous options, but it looks promising.

- [**Protégé**](https://protege.stanford.edu/)
  - It is a widely used ontology (OWL-focused) editor, though a bit buggy.
  - It can be used in combination with a text/code editor by reloading the Protégé session as needed.
  - Ultimately, text/code editors should always be used to write Linked Data specifications because they provide higher control and understanding.

- **Ontologies and Vocabularies**

> [!IMPORTANT]
> In my opinion, using some upper/foundational ontology is better than using none to build domain ontologies because upper ontologies provide essential modeling blocks that you, as a modeler, cannot avoid. Even if you do not explicitly adopt a specific upper ontology, your ontology design will implicitly assume upper ontological distinctions.
>
> Some may argue that certain projects do not need the complexity of a foundational ontology. I agree. However, I would also add that these projects probably do not need to adopt Semantic Web standards either. Sometimes, a list of terms and definitions in CSV suffices.

  - [**gUFO**](https://nemo-ufes.github.io/gufo/)
    - gUFO (to become an [ISO standard](https://www.iso.org/standard/89915.html) soon) is a lightweight implementation of the Unified Foundational Ontology suitable for Semantic Web OWL 2 DL applications. gUFO is the most expressive upper ontology out there, made by computer science folks with philosophical knowledge.
    - The [Basic Formal Ontology](https://github.com/BFO-ontology) (ISO/IEC 21838-2:2021) is another well-known upper ontology, widely used in the biomedical domain, although it is not as complete as gUFO.
  - [**PROV-O**](https://www.w3.org/TR/prov-o/)
    - It is a widely used provenance ontology, a W3C standard.
  - [**DCAT**](https://www.w3.org/TR/vocab-dcat-3/)
    - DCAT-3 is a W3C standard vocabulary for describing data catalogs and their contents on the Web.
  - [**DCMI Metadata Terms**](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/)
    - The Dublin Core Terms (ISO 15836-1:2017, IETF RFC 5013, ANSI/NISO Z39.85) are a widely used standard vocabulary to describe metadata of resources, such as documents, datasets, images, websites, or services.
  - [**SKOS**](https://www.w3.org/2004/02/skos/)
    - SKOS is a W3C standard for representing thesauri and taxonomies, which are much less complex than full-fledged domain ontologies.

# Others

- [**Awesome Semantic Web**](https://github.com/semantalytics/awesome-semantic-web)
  - A miscellaneous list of resources related to Linked Data.
- [**RDF Playground**](https://rdfplayground.dcc.uchile.cl/)
  - For quick interaction with RDF data and SHACL shapes.
