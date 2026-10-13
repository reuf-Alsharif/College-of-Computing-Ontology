# College of Computing Ontology

**Knowledge Representation and Automated Reasoning Using OWL, Protégé, and SPARQL**

## Project Overview

This project presents an OWL ontology designed to represent the organizational structure and academic activities of the College of Computing at Umm Al-Qura University.

Developed using Protégé, the ontology models academic entities and their relationships in a structured, machine-interpretable knowledge base. It demonstrates how semantic technologies can support knowledge representation, logical consistency checking, automated inference, and structured information retrieval.

## Project Objectives

- Model the academic structure of the College of Computing.
- Represent relationships between departments, programs, courses, students, faculty, committees, events, and facilities.
- Define logical constraints and class relationships using OWL.
- Apply automated reasoning to infer implicit knowledge.
- Retrieve and analyze information using SPARQL queries.

## Ontology Design

### Class Hierarchy (TBox)

The ontology defines 10 domain-relevant classes, including:

- College
- Department
- Program
- Course
- Person
- Student
- Faculty
- Committee
- Event
- Facility

The `Student` and `Faculty` classes are modeled as subclasses of `Person`, demonstrating inheritance and specialization.

### Object Properties

The ontology defines 12 object properties to represent relationships between entities, including:

- `hasDepartment`
- `offersProgram`
- `offersCourse`
- `enrolledIn`
- `hasStudent`
- `teaches`
- `taughtBy`
- `memberOf`
- `participatesIn`
- `locatedIn`

Inverse properties support bidirectional relationship inference, while functional properties represent relationships with defined constraints.

### Data Properties

Seven data properties describe entity attributes, including names, email addresses, student IDs, course codes, credit hours, college websites, and event dates. Appropriate datatypes are assigned to support consistent data representation.

## Logical Constraints and Inference

The ontology incorporates several OWL constructs:

- **Disjointness:** Student and Faculty are declared disjoint classes.
- **Cardinality restrictions:** Departments must offer at least one program, programs must offer at least one course, and students can enroll in a maximum of five courses.
- **Defined classes:** `ActiveStudent`, `PopularCourse`, and `DepartmentWithPrograms` use logical conditions to enable automatic classification.

## Automated Reasoning

The HermiT reasoner was used to check logical consistency and demonstrate automated inference.

The reasoning process supports:
- Automatic classification of students enrolled in at least one course as `ActiveStudent`.
- Classification of departments offering programs as `DepartmentWithPrograms`.
- Inference of inverse relationships, such as identifying enrolled students from course enrollment assertions.

The report confirms that the ontology passed the consistency check.

## SPARQL Querying

A collection of **14 SPARQL queries** was developed to demonstrate information retrieval and knowledge analysis.

The queries cover:
- Student information and complete profiles.
- Committee membership analysis.
- Courses filtered by credit hours.
- Student-course-club relationships.
- Events and participants.
- Department-program-course hierarchies.
- Course enrollment statistics.
- Student activity and engagement metrics.

The queries demonstrate features such as `SELECT`, `FILTER`, `OPTIONAL`, `GROUP BY`, `COUNT`, `COUNT DISTINCT`, and `ORDER BY`.

## Project Summary

| Component | Implementation |
|---|---|
| Ontology language | OWL |
| Development environment | Protégé |
| Classes | 10 |
| Object properties | 12 |
| Data properties | 7 |
| Individuals | 25 |
| Defined classes | 3 |
| SPARQL queries | 14 |
| Reasoner | HermiT |

## Technology Stack

- **Ontology Development:** Protégé
- **Knowledge Representation:** OWL
- **Automated Reasoning:** HermiT
- **Query Language:** SPARQL
- **Semantic Web Standards:** W3C OWL 2 and SPARQL 1.1

## Repository Contents

- `README.md` — Project overview and documentation.
- `College_of_Computing_Ontology.owx` — Ontology file, if included.
- `College_of_Computing_Ontology_Report.pdf` — Project report, if included.
- `screenshots/` — Selected ontology and query-result screenshots, if included.

## Future Improvements

Potential extensions include expanding the ontology with additional academic entities, incorporating more comprehensive institutional data, developing a user-friendly query interface, and integrating the ontology into an academic information system.

## Academic Context

**Course:** DS2203 – Knowledge Representation and Inference

**Department:** Data Science Department

**College:** College of Computing, Umm Al-Qura University

**Development Date:** June 2026

