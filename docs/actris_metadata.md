# ACTRIS metadata elements

## MD_metadata

Metadata related to the metadata

### Metadata specific metadata

| Metadata Element Name | Metadata Element REST API syntax | Data type | Description                                                                                                                               | Example                                                              |
|-----------------------|----------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| fileIdentifier        | file_identifier                  | string    | Unique identifier for this metadata file, following internal file naming convention                                                       | Mission.Sensor.Level.Specie.geoID.ProcessinLevel.Version.yyyymmdd.nc |
| language              | language                         | string    | language used for documenting metadata (WIS requires english ""en"")                                                                      | en                                                                   |
| characterSet          | character_set                    | string    | Full name of the character coding standard used for the metadata set                                                                      | utf8                                                                 |
| hierarchyLevel        | hierarchy_level                  | string    | scope to which the metadata applies: (WIS requires ""dataset"" or ""series"", where ""series"" describes a collection of single datasets) | dataset                                                              |
| datestamp             | datestamp                        | date      | date that the metadata was created                                                                                                        | 2012-05-20T09:45:00)                                                 |

### Contact

| Metadata element name | Metadata Element REST API syntax | Data Type | Description                                                                                                      | Example                                                                                                       |
|-----------------------|----------------------------------|-----------|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| individualName        | individual_name                  | string    | name of the responsible person within WDC host organisation: surname, given name, title separated by a delimiter | Fiebig, Markus, Dr.                                                                                           |
| organisationName      | organisation_name                | string    | name of WDC host organisation                                                                                    | Norwegian Institute for Air Research                                                                          |
| positionName          | position_name                    | string    | role or position of the responsible person within WDC host organisation (function, division)                     | Senior Scientist, Dept. Atmospheric and Climate Research (ATMOS), Norwegian Institute for Air Research (NILU) |
| RoleCode              | role_code                        | string    | function performed by the WDC host organisation (select from dropdown list)                                      | custodian                                                                                                     |
| deliveryPoint         | delivery_point                   | string    | street name and number                                                                                           | Instituttveien 18                                                                                             |
| AddressCity           | address_city                     | string    | city                                                                                                             | Kjeller                                                                                                       |
| administrativeArea    | administrative_area              | string    | state, province                                                                                                  | Viken                                                                                                         |
| postalCode            | postal_code                      | string    | ZIP or other postal code                                                                                         | 2007                                                                                                          |
| country               | country                          | string    | country                                                                                                          | Norway                                                                                                        |
| electronicMailAddress | email                            | string    | email address of the responsible organization or individual                                                      | some.name@email.com                                                                                           |

### Online Resource

| Metadata element name | Metadata Element REST API syntax | Data Type | Description                    | Example              |
|-----------------------|----------------------------------|-----------|--------------------------------|----------------------|
| linkage               | linkage                          | URL       | web address of the data center | http://ebas.nilu.no/ |


## MD_DataIdentification

Metadata related to the dataset.

| Metadata element name | Metadata element REST API syntax | Data type      | Description                                                                                                    | Example                                                                                                                                                                                           |
|-----------------------|----------------------------------|----------------|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract              | abstract                         | string         | short description of the dataset described (abstract)(e.g.: parameter, method, instrument, interval, site etc) | Ground based in situ observations of particle_number_size_distribution at Zeppelin mountain (Ny-Ålesund) (NO0042G) using dmps. Parameters measured are: particle_number_size_distribution in pm1. |
| title                 | title                            | string         | name by which the cited reference is known                                                                     | EBAS.<station code>.<start date / time>.<revision date / time>.<component>.<matrix>.<period code>.<resolution code>.<data level>                                                                  |
| identifier            | identifier                       | string         | value uniquely identifying an object within a namespace. DOI of the dataset, if available                      | https://doi.org/10.21336/gen.2                                                                                                                                                                    |
| date                  | date                             | date           | reference date of the dataset                                                                                  | yyyy-mm-ddThh-mm-ss                                                                                                                                                                               |
| dateType              | date_type                        | CodeList B.5.2 | event used for reference date                                                                                  | revision                                                                                                                                                                                          |

### Contact

| Metadata element name | Metadata Element REST API syntax | Data Type | Description                                                                                                      | Example                                                                                                       |
|-----------------------|----------------------------------|-----------|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| individualName        | individual_name                  | string    | name of the responsible person within WDC host organisation: surname, given name, title separated by a delimiter | Fiebig, Markus, Dr.                                                                                           |
| organisationName      | organisation_name                | string    | name of WDC host organisation                                                                                    | Norwegian Institute for Air Research                                                                          |
| positionName          | position_name                    | string    | role or position of the responsible person within WDC host organisation (function, division)                     | Senior Scientist, Dept. Atmospheric and Climate Research (ATMOS), Norwegian Institute for Air Research (NILU) |
| RoleCode              | role_code                        | string    | function performed by the WDC host organisation (select from dropdown list)                                      | custodian                                                                                                     |
| deliveryPoint         | delivery_point                   | string    | street name and number                                                                                           | Instituttveien 18                                                                                             |
| AddressCity           | address_city                     | string    | city                                                                                                             | Kjeller                                                                                                       |
| administrativeArea    | administrative_area              | string    | state, province                                                                                                  | Viken                                                                                                         |
| postalCode            | postal_code                      | string    | ZIP or other postal code                                                                                         | 2007                                                                                                          |
| country               | country                          | string    | country                                                                                                          | Norway                                                                                                        |
| electronicMailAddress | email                            | string    | email address of the responsible organization or individual                                                      | some.name@email.com                                                                                           |

### Online Resource

| Metadata element name | Metadata Element REST API syntax | Data Type | Description                    | Example              |
|-----------------------|----------------------------------|-----------|--------------------------------|----------------------|
| linkage               | linkage                          | URL       | web address of the data center | http://ebas.nilu.no/ |

## MD_Constraints

	> accessConstraints
	> useConstraints
	> otherConstraints
	* How to get access, check with metadata elements in the WIS profile

## MD_Keywords

	> keyword
	> type

## MD_DataIdentification

	> language
	> characterSet
	> topicCategory
	> description

	> Station WMO region
	> Country
	> Station name
	> Station GAW-ID/ACTRIS ID

## EX_Extent

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
	
### dataLicence
	* machine-reable
	* optional, check with WIS profile how to give licence information


### metadataLicence

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
