# ACTRIS metadata elements

## MD_metadata

Metadata related to the metadata

### Metadata specific metadata

| Metadata Element Name | Metadata Element REST API syntax | Data type | Description                                                                                                                               | Example                                                              |
|-----------------------|----------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| fileIdentifier        | file_identifier                  | string    | Unique identifier for this metadata file, following internal file naming convention                                                       | Mission.Sensor.Level.Specie.geoID.ProcessinLevel.Version.yyyymmdd.nc |
| language              | language                         | string    | language used for documenting metadata (WIS requires english ""en"")                                                                      | en                                                                   |
| characterSet          | character_set                    | string    | Full name of the character coding standard used for the metadata set                                                                      | utf8                                                                 |
| hierarchyLevel        | hierarchy_level                  | string    | scope to which the metadata applies: "dataset"" or ""series"", where ""series"" describes a collection datasets 						   | dataset                                                              |
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

| Metadata Element Name | Metadata Element REST API syntax | Data type | Description                                                                                 | Example                                     |
|-----------------------|----------------------------------|-----------|---------------------------------------------------------------------------------------------|---------------------------------------------|
| accessConstraints     | CodeList B.5.24                  | string    | access constraints of the published data                                                    | otherRestrictions                           |
| useConstraints        | CodeList B.5.24                  | string    | any special restrictions or limitations or warnings on using the data                       | otherRestrictions                           |
| otherConstraints      | string                           | string    | other restrictions and legal prerequisites for accessing and using the resource or metadata | https://www.gaw-wdca.org/Browse-Obtain-Data |
| dataLicence           | data_licence                     | string    | fixed list of available licences                                                            | To be decided                               |
| metadataLicence       | metadata_licence                 | string    | fixed list of available licences                                                            | To be decided                               |

## MD_Keywords

| Metadata Element Name | Metadata Element REST API syntax | Data type | Description                                                                          | Example                           |
|-----------------------|----------------------------------|-----------|--------------------------------------------------------------------------------------|-----------------------------------|
| keyword               | keyword                          | string    | keyword(s) describing the theme of the dataset, preferably from the WMO keyword list | Aerosol, Atmospheric, Measurement |

## MD_DataIdentification

| Metadata element name | Metadata element REST API syntax | Data type       | Description                                                     | Example                                      |
|-----------------------|----------------------------------|-----------------|-----------------------------------------------------------------|----------------------------------------------|
| language              | language                         | string          | language used within the dataset                                | en                                           |
| characterSet          | character_set                    | CodeList B.5.10 | full name of the character coding standard used for the dataset | utf8                                         |
| topicCategory         | topic_category                   | CodeList B.5.27 | main theme(s) of the dataset                                    | climatologyMeteorologyAtmosphere             |
| description           | description                      | string          | description of spatial and temporal extent for the dataset      | time series of point measurements at surface |
| code                  | station_wmo_region               | string          | Station WMO region                                              | VI - Europe                                  |
| code                  | country_name                     | string          | country the measurement site is located in (in english)         | Norway                                       |
| code                  | station_name                     | string          | Name of station, platform or observatory                        | Birkenes                                     |
| code                  | station_identifier               | string          | Identifier of station/observatory based on GAW-ID               | BIR                                          |

## GeographicBoundingBox

| Metadata element name | Metadata element REST API syntax | Data type | Description                                                                                                                            | Example |
|-----------------------|----------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|---------|
| westBoundLongitude    | west_bound_longitude             | decimal   | western-most coordinate of the limit of the dataset extent (bounding box), expressed in longitude in decimal degrees (positve east)    | +3.12   |
| eastBoundLongitude    | east_bound_longitude             | decimal   | eastern-most coordinate of the limit of the dataset extent (bounding box), expressed in longitude in decimal degrees (positve east)    | +3.13   |
| southBoundLatitude    | south_bound_latitude             | decimal   | southern-most coordinate of the limit of the dataset extent (bounding box), expressed in longitude in decimal degrees (positve northt) | +42.25  |
| northBoundLatitude    | north_bound_latitude             | decimal   | northern-most coordinate of the limit of the dataset extent (bounding box), expressed in longitude in decimal degrees (positve north)  | +42.26  |

## Temporal extent
	
| Metadata element name | Metadata element REST API syntax | Data type | Description        | Example             |
|-----------------------|----------------------------------|-----------|--------------------|---------------------|
| TimePeriodBegin       | time_period_begin                | date      | dataset start time | yyyy-mm-ddThh-mm-ss |
| TimePeriodEnd         | time_period_end                  | date      | dataset end time   | yyyy-mm-ddThh-mm-ss |

## Vertical extent

| Metadata element name | Metadata element REST API syntax | Data type | Description                                                                  | Example                       |
|-----------------------|----------------------------------|-----------|------------------------------------------------------------------------------|-------------------------------|
| minimumValue          | minimum_value                    | Real      | lowest vertical extent contained in the dataset (altitude of the instrument) | station altitude + height agl |
| maximumValue          | maximum_value                    | Real      | highest vertical extent contained in the dataset (reach of instrument)       | station altitude + height agl |
| unitOfMeasure         | unit_of_measure                  | String    | unit of measure (→WIS requires "m above sea level")                          | m above sea level             |

## Content information

| Metadata element name | Metadata element REST API syntax | Data type      | Description                                                                   | Example             |
|-----------------------|----------------------------------|----------------|-------------------------------------------------------------------------------|---------------------|
| attributeDescription  | attribute_description            | string         | parameter name                                                                | air_temperature     |
| contentType           | content_type                     | CodeList B5.12 | type of information represented by the cell value (select from dropdown list) | physicalMeasurement |


### Distribution informaition (online resource)

	> name of data format
	> version - version number of the transfer format
	> transfer size
	> linkage	URL
	> protocol	String
	> description	String
	> function	CodeList B.5.3
 	> isRestricted 
			* True/False
		* Description

## Data quality information

### DQ_Scope		
	> level 	CodeList B.5.25
### LI_Lineage		
	> statement	String
### LI_ProcessStep		
	> description	String

## Other

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

### data product
	* absorption-spectra, growth factor ++
	
### Property instead of variable?
	* In ACTRIS, DMP is calling everything ACTRIS variables, but need to discuss this
