# Cisco Threat Intel Model (CTIM)

## Description

CTIM, the data model of [CTIA](https://github.com/threatgrid/ctia), is
closely based on [STIX](http://stixproject.github.io/data-model/) with
a few simplifications:

  * The base Types cannot be documented inside of each other.  It's
  like always having to use an _idref_.  This is because we intend to
  build a hypermedia threat intel web combining global and local
  threat intel.

  * It's built on top of a "verdict service" so we simplify
  Observables into their most commonly observed properties.  You no
  longer have to say, "a file, with the sha256 checksum equal to X"
  you would simple say, "a sha256 checksum".  We cross index
  everything on these observables, and distill the indicators down
  into verdicts that allow quick looking to see if an observable is
  of interest.

  * We flatten some structured data to make it easier to deal with as
  JSON and simpler, since we are dealing with specific cases in CTIA.
  We will use default vocabularies whenever they are available.

  * We assume specific string representations for descriptions and
  such, instead of the more complex structured data which allows the
  specification of multiple formats.  This is to enforce a more secure
  representation format suitable for embedding in web applications.

## Models

- [Actor](structures/actor.md)
- [Attack Pattern](structures/attack_pattern.md)
- [Campaign](structures/campaign.md)
- [Course of Action](structures/coa.md)
- [Feedback](structures/feedback.md)
- [Incident](structures/incident.md)
- [Indicator](structures/indicator.md)
- [Judgement](structures/judgement.md)
- [Malware](structures/malware.md)
- [Relationship](structures/relationship.md)
- [Casebook](structures/casebook.md)
- [Sighting](structures/sighting.md)
- [IdentityAssertion](structures/identity_assertion.md)
- [Tool](structures/tool.md)
- [Verdict](structures/verdict.md)
- [Weakness](structures/weakness.md)

## Relationships

- [Defined Relationships](defined_relationships.md)

## Graphs

- [Data Model Graph](img/model.png) ([Graphviz `.dot'](graph/model.dot))

## Examples

- [Actor](json/actor.json) JSON
- [Attack Pattern](json/attack_pattern.json) JSON
- [Campaign](json/campaign.json) JSON
- [Course of Action](json/coa.json) JSON
- [Feedback](json/feedback.json) JSON
- [Incident](json/incident.json) JSON
- [Indicator](json/indicator.json) JSON
- [Judgement](json/judgement.json) JSON
- [Malware](json/malware.json) JSON
- [Relationship](json/relationship.json) JSON
- [Casebook](json/casebook.json) JSON
- [Sighting](json/sighting.json) JSON
- [IdentityAssertion](json/identity_assertion.json) JSON
- [Tool](json/tool.json) JSON
- [Verdict](json/verdict.json) JSON
- [Weakness](json/weakness.json) JSON

## Domain Logic

- [Sorting](domain/sorting.md)
