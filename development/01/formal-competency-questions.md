# Formal Competency Questions

## CQ_1.1
What are the preferred terms to identify digitization activities? What are other terms used to identify them?

```sparql
PREFIX abox: <http://purl.org/changes/diva/development/01/data/>
PREFIX tbox: <http://purl.org/changes/diva/development/01/schema/>

SELECT ?pref_label ?alt_label 
WHERE {
    ?activity tbox:hasBroaderConcept abox:digitization-activity ;
              tbox:hasPreferredLabel ?pref_label ;
              tbox:hasAlternativeLabel ?alt_label .
}
```

## CQ_1.2
What are the definitions of digitization activities?

```sparql
PREFIX abox: <http://purl.org/changes/diva/development/01/data/>
PREFIX tbox: <http://purl.org/changes/diva/development/01/schema/>

SELECT ?pref_label ?definition 
WHERE {
    ?activity tbox:hasBroaderConcept abox:digitization-activity ;
              tbox:hasPreferredLabel ?pref_label ;
              tbox:hasDefinition ?definition .
}
```

## CQ_1.3
How are digitization activities hierarchically related to each other?

```sparql
PREFIX abox: <http://purl.org/changes/diva/development/01/data/>
PREFIX tbox: <http://purl.org/changes/diva/development/01/schema/>

SELECT ?activity ?hierarchical_relation ?related_concept 
WHERE {
    ?activity ?hierarchical_relation ?related_concept .
    FILTER(
        ?hierarchical_relation == tbox:hasBroaderConcept ||
        ?hierarchical_relation == tbox:hasNarrowerConcept
    )
}
```

## CQ_1.4
Which external concepts are the digitization activities mapped to?

```sparql
PREFIX abox: <http://purl.org/changes/diva/development/01/data/>
PREFIX tbox: <http://purl.org/changes/diva/development/01/schema/>

SELECT ?activity ?mapping_relation ?related_concept 
WHERE {
    ?activity ?mapping_relation ?related_concept .
    FILTER(
        ?hierarchical_relation == tbox:hasRelatedConcept ||
        ?hierarchical_relation == tbox:hasExactConcept ||
        ?hierarchical_relation == tbox:hasCloseConcept
    )
}
```

## CQ_1.5
Who created each concept representing a digitization activity? When? Why? Which sources were used? 

```sparql
PREFIX abox: <http://purl.org/changes/diva/development/01/data/>
PREFIX tbox: <http://purl.org/changes/diva/development/01/schema/>

SELECT ?activity ?creator ?creation_date ?motivation ?source 
WHERE {
    ?activity tbox:hasBroaderConcept abox:digitization-activity ;
              tbox:hasCreator ?creator ;
              tbox:hasCreationDate ?creation_date ;
              tbox:hasMotivation ?motivation ;
              tbox:hasSource ?source .
}
```