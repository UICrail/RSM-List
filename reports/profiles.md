# OWL Profile Validation Report

**Ontology**: ontology/src/list2.ttl
**Date**: 2026-06-26 06:17:19 UTC

---

## OWL2 DL Profile

✅ **Status**: PASSED

```
OWL 2 DL Profile Report: [Ontology and imports closure in profile]
```

## OWL2 RL Profile

⚠️ **Status**: VIOLATIONS DETECTED

```
OWL 2 RL Profile Report: Ontology and imports closure NOT in profile. The following violations are present:
Use of non-superclass expression in position that requires a superclass expression: ObjectSomeValuesFrom(<https://w3id.org/list#hasNext> <https://cdm.ovh/rsm/list2/list2#ListNode>) [SubClassOf(<https://w3id.org/list#OWLList> ObjectSomeValuesFrom(<https://w3id.org/list#hasNext> <https://cdm.ovh/rsm/list2/list2#ListNode>)) in OntologyID(OntologyIRI(<https://cdm.ovh/rsm/list2>) VersionIRI(<https://cdm.ovh/rsm/list2/0.1/list2>))]
```
