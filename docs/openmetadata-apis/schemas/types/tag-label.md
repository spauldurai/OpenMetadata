# Tag Label

This schema defines the type for labeling an entity with a Tag.

**$id:** [**https://github.com/open-metadata/OpenMetadata/blob/main/catalog-rest-service/src/main/resources/json/schema/type/tagLabel.json**](https://github.com/open-metadata/OpenMetadata/blob/main/catalog-rest-service/src/main/resources/json/schema/type/tagLabel.json)

Type: `object`

## Properties

* **tagFQN**
  * Type: `string`
  * Length:  ≤ 45
* **labelType**
  * Label type describe how a tag label was applied. 'Manual' indicates the tag label was applied by a person. 'Derived' indicates a tag label was derived using associated tag relationship \(see TagCategory.json for more details\). 'Propagated\` indicates a tag label was propagated from upstream based on lineage. 'Automated' is used when a tool was used to determine the tag label.
  * Type: `string`
  * The value is restricted to the following: 
    1. _"Manual"_
    2. _"Propagated"_
    3. _"Automated"_
    4. _"Derived"_
  * Default: _"Manual"_
* **state**
  * 'Suggested' state is used when a tag label is suggested by users or tools. Owner of the entity must confirm the suggested labels before it is marked as 'Confirmed'
  * Type: `string`
  * The value is restricted to the following: 
    1. _"Suggested"_
    2. _"Confirmed"_
  * Default: _"Confirmed"_
* **href**
  * Link to the tag resource.
  * $ref: [basic.json\#/definitions/href](tag-label.md#basic.jsondefinitionshref)
