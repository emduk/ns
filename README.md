# EMD UK Extension Namespace Vocabulary Terms

This repository holds the [JSON-LD definition](http://data.emduk.org/ns/emduk.jsonld) of the "emduk" namespace.

This namespace can be used by publishers wanting to experiment with new properties that EMD UK are using in addition to the core [Modelling Opportunity Data Specification](https://www.openactive.io/modelling-opportunity-data/). Publishers should not assume that properties in this namespace will either be added to the core specification or be stable over the long term, as they exist primarily for the use of EMD UK.

EMD UK works as part of the [OpenActive Community Group](https://www.w3.org/community/openactive) to promote the usecases represented by the properties within this namespace, with the intention of standardising them over time.

This namespace MUST be referenced using the URL `"http://data.emduk.org/ns/emduk.jsonld"` (which will return the [JSON-LD definition](http://data.emduk.org/ns/emduk.jsonld)), and is designed to be used in conjunction with the `"https://openactive.io/"` namespace.

Please raise requests for content or issues related to the namespace via [GitHub](https://github.com/emduk/ns/issues). 

Recommended usage as follows:
```json
{
  "@context": [
    "https://openactive.io/",
    "http://data.emduk.org/ns/emduk.jsonld"
  ],
  "type": "SessionSeries",
  "name": "Tai chi Class",
  "url": "http://www.example.org/events/1",
  "emduk:isWheelchairAccessible": true,
  "location": {
    "type": "Place",
    "name": "ExampleCo Gym Kingswood",
    "address": {
      "type": "PostalAddress",
      "streetAddress": "1 High Street",
      "addressLocality": "Kingswood",
      "addressRegion": "South Gloucestershire",
      "postalCode": "BS1 4SD",
      "addressCountry": "GB"
    }
  }
}
```



## Properties

| (Class) Property    |  Expected Type  | Proposal   | Description                                                         |
|---------------------|-----------------|------------|---------------------------------------------------------------------|
| ([`schema:Event`](https://schema.org/Event)) <br/> `emduk:isWheelchairAccessible` | [`schema:Boolean`](https://schema.org/Boolean) | [#166](https://github.com/openactive/modelling-opportunity-data/issues/166) | A property that details whether the event is suitable for wheelchair access. Placed on Event as this field could be used to detail whether the Event is suitable, as well as the Place. |
| ([`schema:Event`](https://schema.org/Event)) <br/> `emduk:specialRequirements` | [`skos:Concept`](http://www.w3.org/2004/02/skos/core#Concept) | [#67](https://github.com/openactive/modelling-opportunity-data/issues/67) | List of related special requirements from the controlled vocabulary http://data.emduk.org/special-requirements/. |

