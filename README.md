# Conceptual Modeling and Linked Data Tools

An opinionated list of useful tools for Conceptual Modeling and Linked Data.


# Conceptual Modeling

Conceptual Modeling is the activity of formally describing some aspects of the physical and social world around us for purposes of understanding and communication. Conceptual models are intended to be used by humans, not machines, although they can support computational tasks, such as data model design and automated reasoning. The need for conceptual models is, therefore, a human need to understand the environment by a form of intersubjective representation (very often a diagrammatic form).

Modeling the domain or the problem correctly is one of the most important tasks in a project, if not the most important one, because grasping things incorrectly yields bad implementation and future interoperability issues.

- [OntoUML plugin for Visual Paradigm](https://github.com/OntoUML/ontouml-vp-plugin)
  - Visual Paradigm is a professional conceptual modeling toolsuite. The [community edition](https://www.visual-paradigm.com/editions/community/) can be used for free for non-commercial purposes.
  - The OntoUML is, in practice, a UML Class diagram profile, whose grammar is designed according to the Unified Foundational Ontology. Consequently, the OntoUML models are constrained by useful upper ontological distinctions, preventing certain modeling mistakes by design.
  - Furthermore, the OntoUML plugin includes several services, such as syntax verification and OWL generation (based on [gUFO](https://nemo-ufes.github.io/gufo/)). This way, it is possible to build a diagrammatic model and obtain its Linked Data implementation automatically.
  - A detailed catalog of OntoUML models can be found [**here**](https://github.com/OntoUML/ontouml-models).

- [Mermaid](https://github.com/mermaid-js/mermaid)
  - Mermaid is a free, open-source, easy-to-use tool for diagram generation with a Markdown-like textual syntax, supporting flow charts, various UML diagrams, ER diagrams, and many more.

- [PlantUML](https://github.com/plantuml/plantuml)
  - PlantUML is similar to Mermaid, but more powerful, although it is also more difficult to use.

- [Archi](https://github.com/archimatetool/archi)
  - Archi is a free, open-source tool for [ArchiMate](https://en.wikipedia.org/wiki/ArchiMate), a standard language for Enterprise Architecture.

# Linked Data

By "Linked Data", we mean tools related to [Semantic Web standards](https://www.w3.org/2001/sw/wiki/Main_Page), particularly RDF, RDFS, OWL, SPARQL, and SHACL.

- [W3ID](https://github.com/perma-id/w3id.org)
  - Free, opens-source, secure, permanent URLs for Web applications. It is the best service of this kind.
  - The purl.archive is another example, easier to use, but much less reliable. Services that generate [DOIs](https://www.doi.org/), such as Zenodo, have a different purpose, not suitable for Linked Data applications.

- [ReSpec](https://github.com/speced/respec)
  - ReSpec is a JS library that makes it easier to write technical specifications, or documents that tend to be technical in nature in general. It was originally designed for the purpose of writing W3C specifications.

- [The FAIR Cookbook](https://github.com/FAIRplus/the-fair-cookbook)
  - Recipes to produce information artifacts that are **F**indable, **A**ccessible, **I**nteroperable, and **R**eusable.

- [RDFlib](https://github.com/RDFLib)
  - The best Python library and ecosystem for Linked Data.
  - The JavaScript analogous is [rdflib.js](https://github.com/linkeddata/rdflib.js).

- Triplestores
  - Only open-source, free recommendations.
  - [Jena Fuseki Server with Inference Support](https://github.com/andybywire/jena-fuseki-inf)
    - Docker image for running Apache Jena Fuseki with RDFS and OWL inference. The easiest and fastest way to run Fuseki.
  - [Qlever](https://github.com/ad-freiburg/qlever)
  - [Oxigraph](https://github.com/oxigraph/oxigraph)

- Ontologies
  - [gUFO](https://nemo-ufes.github.io/gufo/)
    - Using some upper ontology is better than using none. However, gUFO is the richest option out there, made by computer science folks with philosophical knowledge.
  - [PROV-O](https://www.w3.org/TR/prov-o/)
    - Widely used provenance ontology, a W3C standard.
  - [DCAT](https://www.w3.org/TR/vocab-dcat-3/)
  - [DCMI Metadata Terms](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/)
  - [Semantic Sensor Network Ontology](https://www.w3.org/TR/vocab-ssn/)
  - [SKOS](https://www.w3.org/2004/02/skos/)
    - Good for taxonomies, bad for everything else.

# Others

- [Awesome Semantic Web](https://github.com/semantalytics/awesome-semantic-web)
  - Miscellaneous list of resources related to Linked Data.