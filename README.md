# Purpose

Linked list ontology for all purposes.

# Source

This ontology is derived from the ontology developed by Pauwels & Terkaj,  originally published by Drummond et al., with namespace http://www.co-ode.org/ontologies/lists/2008/09/11/list.owl# and available at web location http://owl.cs.manchester.ac.uk/wp-content/uploads/2015/07/list.owl_.txt on 11 December 2015.

The main changes are OWL2 RL compliance and the changed handling of EmptyList, for which an individual is also provided.

The original terminology was kept.

# How it works

It is based on a linked list paradigm, by which any element has a successor, and possibly a payload.

An "empty list" individual is provided to close the list, if desired.

# Closed list?

The OWL ontology does not require each list node (except the terminal 'empty list') to have a successor. This is because the OWL2 RL profile excludes existential restrictions in superclass expressions.

If it is necessary to enforce closed lists, the user may use any of the solutions below:

* add the existential restriction and accept OWL2 DL compliance;
* use the provided SHACL shape;
* state that non-functional property isFollowedBy (the transitive closure of hasNext) has value, inter alia, emptyList:

list:OWLList rdfs:subClassOf
    [ rdf:type owl:Restriction ;
      owl:onProperty list:isFollowedBy> ;
      owl:hasValue list:emptyList
    ] .

Latter formulation is definitely RL-compliant, but we leave it to the user to enforce list closure.
