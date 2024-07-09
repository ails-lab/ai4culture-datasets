# ai4culture-datasets

The datasets include textual descriptions of Europeana metadata records annotated with terms (URIs) from Wikidata. Those terms may represent concepts (such as jewellery) or named entities (such as person names and locations). All annotations are validated by humans. The textual descriptions include text in the following languages:  English, Dutch, Swedish, and Spanish.
  
The metadata have been sourced from Europeana in the context of (expert) crowdsourcing campaigns during the EuropeanaXX and CRAFTED projects and originate from the following  aggregators and providers: EuropeanaFashion, EUScreen, Photoconsortium, and European Film Gateway.

The following criteria have been applied for including an annotation (i.e. pairs of textual values and URIs/terms) in the dataset:
- We only consider annotations that have been marked as “accepted” by the majority of humans who reviewed them.
- We only consider annotations referring to the textual values of the dc:description metadata field.
- Each distinct term/URI appears up to 30 times per considered language, i.e. in up to 30 different dc:description values.

From a technical point of view, the annotated data are structured in the form of four TSV files, one per considered language. The files are UTF-8 encoded, with the following headers:

- ORIGINAL_VALUE: the full text in the field dc:description
- LANGUAGE: the language of the ORIGINAL_VALUE
- URI: the Wikidata URI to which the substring of ORIGINAL_VALUE starting at position START and ending at position END has been linked to
- START: the starting character position of the identified string within the ORIGINAL_VALUE
- END: the end character position of the identified string within the ORIGINAL_VALUE
