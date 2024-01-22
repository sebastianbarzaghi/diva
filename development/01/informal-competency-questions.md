# Informal Competency Questions

## Identifier
CQ_1.1

## Labeling question
What are the preferred terms to identify digitization activities? What are other terms used to identify them?

## Expected result
List: `pref_label`, `alt_label`

## Expected result
* "Acquisition", "Data capture"
* "Processing", "Data processing"
* "Modelling", "3D modelling"
* "Optimization", "3D model optimization"
* "Export", "Data export"
* "Description metadata creation", "Metadata creation"
* "Provenance metadata creation", "Provenance creation"
* "Upload", "3D model upload"

***

## Identifier
CQ_1.2

## Documentation question
What are the definitions of digitization activities?

## Expected result
List: `pref_label`, `definition`

## Expected result
* "Acquisition", "A digitization activity meant to capture analogue materials and acquire their digital representation";
* "Processing", "A digitization activity meant to manipulate digital files in order to facilitate further operations on them";
* "Modelling", "A digitization activity meant to bring together digital files in order to create a fully-fledged 3D model";
* "Optimization", "A digitization activity to optimise a digital 3D model for specific purposes or use cases";
* "Export", "A digitization activity meant to convert the digital files into a specific format";
* "Description metadata creation", "A digitization activity meant to create structured metadata describing the content and context of the digital files";
* "Provenance metadata creation", "A digitization activity meant to create provenance metadata to track the agent responsible for data creation, the time of data creation, and the primary source of the data";
* "Upload", "A digitization meant to transfer digital 3D models from a local device or storage location to a Web-based framework".

***

## Identifier
CQ_1.3

## Semantic relations question
How are digitization activities hierarchically related to each other?

## Expected result
List: `activity`, `hierarchical_relation`, `related_concept`

## Expected result
* `acquisition`, `hasBroaderConcept`, `digitization-activity`
* `processing`, `hasBroaderConcept`, `digitization-activity`
* `modelling`, `hasBroaderConcept`, `digitization-activity`
* `optimization`, `digitization-activity`
* `export`, `hasBroaderConcept`, `digitization-activity`
* `description-metadata-creation`, `hasBroaderConcept`, `digitization-activity`
* `provenance-metadata-creation`, `hasBroaderConcept`, `digitization-activity`
* `upload`, `hasBroaderConcept`, `digitization-activity`

***

## Identifier
CQ_1.4

## Mapping relations question
Which are external concepts digitization activities are mapped to?

## Expected result
List: `activity`, `mapping_relation`, `related_concept`

# Expected result
* `acquisition`, `hasRelatedConcept`, https://www.wikidata.org/wiki/Q1172399
* `processing`, `hasRelatedConcept`, https://www.wikidata.org/wiki/Q6661985
* `modelling`, `hasRelatedConcept`, https://www.wikidata.org/wiki/Q568742
* `optimization`, `hasRelatedConcept`, https://www.wikidata.org/wiki/Q1156793
* `export`, `hasRelatedConcept`, https://www.wikidata.org/wiki/Q59154708
* `description-metadata-creation`, `hasRelatedConcept`, https://www.wikidata.org/wiki/Q105100083
* `provenance-metadata-creation`, `hasRelatedConcept`, https://www.wikidata.org/wiki/Q105100083
* `upload`, `hasRelatedConcept`, https://www.wikidata.org/wiki/Q7126699

***

## Identifier
CQ_1.5

## Provenance question
Who created each concept representing a digitization activity? When? Why? Which sources were used? 

## Expected result
List: `activity`, `creator`, `creation_date`, `motivation`, `source`

## Expected result
* `acquisition`, https://orcid.org/0000-0002-0799-1527, "2024-01-12T00:00:00Z", "Added to represent the data acquisition activity carried out on an object (e.g. a sculpture, a book, a conversation, etc.) through the use of hardware and/or software within a digitization workflow", https://doi.org/10.1016/j.daach.2023.e00309
* `processing`, https://orcid.org/0000-0002-0799-1527, "2024-01-12T00:00:00Z", "Added to represent the data processing activity carried out on some digital files through the use of software within a digitization workflow", https://doi.org/10.1016/j.daach.2023.e00309
* `modelling`, https://orcid.org/0000-0002-0799-1527, "2024-01-12T00:00:00Z", "Added to represent the 3D modelling activity carried out on some digital files through the use of software within a digitization workflow", https://doi.org/10.1016/j.daach.2023.e00309
* `optimization`, https://orcid.org/0000-0002-0799-1527, "2024-01-12T00:00:00Z", "Added to represent the 3D model optimization activity carried out on some 3D model through the use of software within a digitization workflow", https://doi.org/10.1016/j.daach.2023.e00309
* `export`, , https://orcid.org/0000-0002-0799-1527, "2024-01-12T00:00:00Z", "Added to represent the data export activity carried out in a software used to edit some digital artifact within a digitization workflow", https://doi.org/10.1016/j.daach.2023.e00309
* `description-metadata-creation`, https://orcid.org/0000-0002-0799-1527, "2024-01-12T00:00:00Z", "Added to represent the activity of creating descriptive metadata for some physical and/or digital objects within a digitization workflow", https://doi.org/10.1016/j.daach.2023.e00309
* `provenance-metadata-creation`, https://orcid.org/0000-0002-0799-1527, "2024-01-12T00:00:00Z", "Added to represent the activity of creating provenance metadata for some digital records within a digitization workflow", https://doi.org/10.1016/j.daach.2023.e00309
* `upload`, https://orcid.org/0000-0002-0799-1527, "2024-01-12T00:00:00Z", "Added to represent the activity of uploading some digital object on a publication platform within a digitization workflow", https://doi.org/10.1016/j.daach.2023.e00309
