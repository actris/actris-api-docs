# ACTRIS metadata elements

## General metadata

	> fileIdentifier
	> language
	> characterSet

	> hierarchyLevel

	> dateStamp
	> metadataStandardName
	> metadataStandardVersion

## Contact information data center unit

### Responsible party
	> individualName
	> organisationName
	> positionName
	> RoleCode

### Address

	> deliveryPoint
	> Address.city
	> administrativeArea
	> postalCode
	> country
	> electronicMailAddress

### Online Resource

	> linkage

## identification information

	> abstract
	> title
	> identifier
	> date
	> dateType

### Responsible party

	> individualName
	> organisationName
	> positionName
	> role 

### Address

	> deliveryPoint
	> Address.city
	> administrativeArea
	> postalCode
	> country
	> electronicMailAddress	

### online resource

	> linkage

## legalConstraints

	> accessConstraints
	> useConstraints
	> otherConstraints

## Metadata keywords

	> keyword
	> type

## Data identification

	> language
	> characterSet
	> topicCategory
	> description

	> Station WMO region
	> Country
	> Station name

## EX_GeographicBoundingBox

	> westBoundLongitude
eastBoundLongitude
southBoundLatitude
northBoundLatitude

## Temporal extent
	
	extent
	gml:TimePeriod
	gml:TimePeriodBegin
	gml:TimePeriodEnd

## Vertical extent
	minimumValue
	maximumValue
	unitOfMeasure

## Content information

attributeDescription - component name
contentType

### Coverage information


### Distribution informaition

	name of data format
	version - version number of the transfer format
	transfer size

### Online data resource

	linkage	URL
	protocol	String
	description	String
	function	CodeList B.5.3

## Data quality information

### DQ_Scope		
	level 	CodeList B.5.25
### LI_Lineage		
	statement	String
### LI_ProcessStep		
	description	String

## What do we need in addition to this?
 - What about transfer of level 3 metadata?


