# ACTRIS metadata elements

## General metadata

| Metadata  Name |	DataType |	Obligation | Description | Reference | Example |
|----------------|----------|-------------|-------------|-----------|---------|
|	file identifier	   | string	  |          |             |             |           |         |


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
	* How to get access, check with metadata elements in the WIS profile

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
	> Station GAW-ID/ACTRIS ID

## EX_GeographicBoundingBox

	> westBoundLongitude
	> eastBoundLongitude
	> southBoundLatitude
	> northBoundLatitude

## Temporal extent
	
	> extent
	> gml:TimePeriod
	> gml:TimePeriodBegin
	> gml:TimePeriodEnd

## Vertical extent
	> minimumValue
	> maximumValue
	> unitOfMeasure

## Content information

	> attributeDescription - component name
	> contentType

### Coverage information


### Distribution informaition

	> name of data format
	> version - version number of the transfer format
	> transfer size

### Online data resource

	> linkage	URL
	> protocol	String
	> description	String
	> function	CodeList B.5.3

## Data quality information

### DQ_Scope		
	> level 	CodeList B.5.25
### LI_Lineage		
	> statement	String
### LI_ProcessStep		
	> description	String

## Specific data center unit metadata (mandatory)

### platform type:
	* Surface station
	* Simulation chamber
	* ballon

### product type:
	* model
	* observation
	* fundamental parameter

### matrix/topic/compartment
	* Fixed list [cloud, gas, particle, met]
	* Change the vocabulary
	* Subject to change (topic, matrix, compartment ...)

### Sub matrix
	* create example list, Markus
	
### Instrument type
	* Fixed list (optional)
	* Multiple entries
	
### program affiliation
	* [GAW-WDCA, EMEP, EUROCHAMP?, NDACC, ARM,] 
	
### legacy data
	* True/False
	* data before ACTRIS RI
	
### data level
	* Fixed list of what is in the DMP

### data sublevel

### isrestricted 
	* True/False
	* Description
	
### licence
	* machine-reable
	* optional, check with WIS profile how to give licence information
	* Include licence on metadata

### data product
	* absorption-spectra, growth factor ++
	
### Property instead of variable?
	* In ACTRIS, DMP is calling everything ACTRIS variables, but need to discuss this

### ASC

### In Situ

### ARES

### CLU

### GRES

### Level 3 data products

## Other
- Consistent metadata element names
- ACTRIS list: Create station list including GAW code and coordinates (from GAWSIS)
