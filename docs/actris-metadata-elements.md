# ACTRIS metadata elements

* [md_metadata](#md_metadata)
* [md_identification](#md_dataidentification)
* [md_constraints](#md_constraints)
* [md_keywords](#md_keywords)
* [md_data_identification](#md_dataidentification-1)
* [ex_geographic_bounding_box](#geographicboundingbox)
* [ex_temporal_extent](#temporal-extent)
* [ex_vertical_extent](#vertical-extent)
* [md_content_information](#content-information)
* [md_distribution_information](#md_distribution_information)
* [dq_data_quality_information](#dq_data_quality_information)
* [md_actris_specific](#md_actris_specific)

## md_metadata

Metadata related to the metadata

| Metadata Element Name | Metadata Element REST API syntax | Data type | Description                                                                                                   | Example                                                              |
|-----------------------|----------------------------------|-----------|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| fileIdentifier        | file_identifier                  | string    | Unique identifier for this metadata file, following internal file naming convention                             | Mission.Sensor.Level.Specie.geoID.ProcessinLevel.Version.yyyymmdd.nc |
| language              | language                         | string    | language used for documenting metadata (WIS requires english ""en"")                                            | en                                                                   |
| characterSet          | character_set                    | string    | Full name of the character coding standard used for the metadata set                                            | utf8                                                                 |
| hierarchyLevel        | hierarchy_level                  | string    | scope to which the metadata applies: "dataset"" or ""series"", where ""series"" describes a collection datasets | dataset                                                              |
| datestamp             | datestamp                        | date      | date that the metadata was created                                                                              | 2012-05-20T09:45:00                                                  |

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


## md_identification

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

## md_constraints

| Metadata Element Name | Metadata Element REST API syntax | Data type | Description                                                                                 | Example                                     |
|-----------------------|----------------------------------|-----------|---------------------------------------------------------------------------------------------|---------------------------------------------|
| accessConstraints     | accessConstraints                  | string    | access constraints of the published data                                                    | otherRestrictions                           |
| useConstraints        | use_constraints                  | string    | any special restrictions or limitations or warnings on using the data                       | otherRestrictions                           |
| otherConstraints      | other_constraints                           | string    | other restrictions and legal prerequisites for accessing and using the resource or metadata | https://www.gaw-wdca.org/Browse-Obtain-Data |
| dataLicence           | data_licence                     | string    | fixed list of available licences                                                            | To be decided                               |
| metadataLicence       | metadata_licence                 | string    | fixed list of available licences                                                            | To be decided                               |

## md_keywords

| Metadata Element Name | Obligation | Data type | Description                                                                          | Example                           |
|-----------------------|----------------------------------|-----------|--------------------------------------------------------------------------------------|-----------------------------------|
| keyword               | mandatory                          | string    | keyword(s) describing the theme of the dataset, preferably from the WMO keyword list | ["NO0042G,", "Zeppelin", "mountain", "(Ny-\u00c5lesund),", "pm10,", "particle_number_size_distribution,", "GAW-WDCA,", "ACTRIS,", "EMEP,", "NILU"] |

## md_data_identification

| Metadata element name | Obligation | Data type       | Description                                                     | Example                                      |
|-----------------------|----------------------------------|-----------------|-----------------------------------------------------------------|----------------------------------------------|
| language              | mandatory                         | string          | language used within the dataset                                | en                                           |
| characterSet          | mandatory                    | CodeList B.5.10 | full name of the character coding standard used for the dataset | utf8                                         |
| topicCategory         | mandatory                   | CodeList B.5.27 | main theme(s) of the dataset                                    | climatologyMeteorologyAtmosphere             |
| description           | mandatory                      | string          | description of spatial and temporal extent for the dataset      | time series of point measurements at surface |
| code                  | mandatory               | string          | Station WMO region                                              | VI - Europe                                  |
| code                  | mandatory                     | string          | country the measurement site is located in (in english)         | Norway                                       |
| code                  | mandatory                     | string          | Name of station, platform or observatory                        | Birkenes                                     |
| code                  | mandatory               | string          | Identifier of station/observatory based on GAW-ID               | BIR                                          |

## ex_geographic_bounding_box

| Metadata element name | Obligation | Data type | Description                                                                                                                            | Example |
|-----------------------|----------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|---------|
| west_bound_longitude    | mandatory             | decimal   | western-most coordinate of the limit of the dataset extent (bounding box), expressed in longitude in decimal degrees (positve east)    | 11.88934   |
| east_bound_longitude    | mandatory             | decimal   | eastern-most coordinate of the limit of the dataset extent (bounding box), expressed in longitude in decimal degrees (positve east)    | 11.88934   |
| south_bound_latitude    | mandatory             | decimal   | southern-most coordinate of the limit of the dataset extent (bounding box), expressed in longitude in decimal degrees (positve northt) | 78.90669  |
| north_bound_latitude    | mandatory             | decimal   | northern-most coordinate of the limit of the dataset extent (bounding box), expressed in longitude in decimal degrees (positve north)  | 78.90669  |

## ex_temporal_extent
	
| Metadata element name | Obligation | Data type | Description        | Example             |
|-----------------------|----------------------------------|-----------|--------------------|---------------------|
| time_period_begin       | mandatory                | date      | dataset start time (ISO 8601) | "2018-01-01T00:00:00" |
| time_period_end         | mandatory                  | date      | dataset end time (ISO 8601)  | 2019-01-01T00:00:00 |

## ex_vertical_extent

| Metadata element name | Obligation | Data type | Description                                                                  | Example                       |
|-----------------------|----------------------------------|-----------|------------------------------------------------------------------------------|-------------------------------|
| minimum_value          | optional                    | Real      | lowest vertical extent contained in the dataset (altitude of the instrument) | null |
| maximum_value          | optional                    | Real      | highest vertical extent contained in the dataset (reach of instrument)       | 475.0 |
| unit_of_measure         | optional                  | String    | unit of measure (→WIS requires "m above sea level")                          | "m above sea level"             |

## md_content_information

| Metadata element name | Obligation | Data type      | Description                                                                   | Example             |
|-----------------------|----------------------------------|----------------|-------------------------------------------------------------------------------|---------------------|
| attribute_description  | mandatory            | string         | parameter name                                                                | ["particle_number_size_distribution"]     |
| content_type           | mandatory                     | CodeList B5.12 | type of information represented by the cell value (select from dropdown list) | "physicalMeasurement" |


## md_distribution_information

| Metadata element name  | Obligation | Data type      | Description                                                                                                                                       | Example                                                                                                                                                                                                                       |
|------------------------|----------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| data_format            | mandatory                      | String         | name of the data transfer format                                                                                                                  | netCDF                                                                                                                                                                                                                        |
| version_data_format    | mandatory              | String         | version of the format (data, number, etc)                                                                                                         | 4                                                                                                                                                                                                                             |
| transfersize           | optional                    | Real           | estimated size of a unit in the specified transfer format, expressed in megabytes. The transfersize is > 0.0                                      | 0.3                                                                                                                                                                                                                           |
| dataset_url            | mandatory                      | URL            | location (address) for on-line access using Uniform Resource Locator address or similar addressing scheme such as http://www.statkart.no/isotc211 | https://thredds.nilu.no/thredds/fileServer/ebas/NO0042G.20171229200000.20190430232636.dmps.particle_number_size_distribution.pm10_non_volatile.16mo.1h.NO01L_DMPS_ZEP1_NRT.NO01L_dmps_DMPS_ZEP02_nonvol__lev0-proc-v0-2-0..nc |
| protocol               | mandatory                        | String         | connection protocol to be used                                                                                                                    | http                                                                                                                                                                                                                          |
| description            | optional                     | String         | detailed text description of what the online resource is/does                                                                                     | Direct download of data file (netCDF)                                                                                                                                                                                         |
| function               | mandatory                         | CodeList B.5.3 | code for function performed by the online resource                                                                                                | download                                                                                                                                                                                                                      |

### restriction
| Metadata element name  | Obligation | Data type      | Description                                                                                                                                       | Example                                                                                                                                                                                                                       |
|------------------------|----------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| set           | mandatory                    | bool           | If authentication is required, True/False                                                                                                         | true                                                                                                                                                                                                                          |
| description_url | optional          | string         | Information on how to get access                                                                                                                  | "https://somepage.com/create_user"                                                                                                                                                                                                |

## dq_data_quality_information

| Metadata element name | Obligation | Data type       | Description                                                                                     | Example                                                                                                                                                      |
|-----------------------|----------------------------------|-----------------|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| level                 | optional                            | CodeList B.5.25 | scope to which the metadata applies:                                                            | dataset                                                                                                                                                      |
| statement             | optional                        | string          | (→WIS requires "dataset" or "series", where "series" describes a collection of single datasets) | Data collected according to instrument specific standard operating procedures, checked on import into data base.                                             |
| description           | optional                      | string          | general explanation of the data producer's knowledge about the lineage of a dataset             | Regularly calibrated by instrument operator, manually quality assured by instrument operator, boundary checked by data centre, outlier check by data centre. |

## md_actris_specific

| Metadata element name    | Obligation | Data type | Description                                                                                 | Example                      |
|--------------------------|----------------------------------|-----------|---------------------------------------------------------------------------------------------|------------------------------|
| platform_type             | mandatory                    | string    | Platform type as fixed list of keywords ['surface_station', 'simulation_chamber', 'ballon'] | "surface_station"              |
| product_type              | mandatory                     | string    | Product type as fixed list of keywords ['model', 'observation', 'fundamental_parameter']    | "observation"                        |
| matrix                    | mandatory         | string    | Matrix as fixed list ['cloud', 'gas', 'particle', 'met']                                    | "particle"                     |
| sub_matrix                | mandatory                       | string    |                                                                                            | "pm10"                            |
| instrument_type           | mandatory                  | string    | Fixed list of instruments                              | "filter_absorption_photometer" |
| program_affiliation       | mandatory              | string    | Fixed list of affiliated programs                                                           | ["EMEP"]                        |
| legacy_data               | mandatory                      | bool      | If data is acquired before the ACTRIS RI was initiated.                                     | false                        |
| data_level                | mandatory                       | int       | Data level as they are defined in the ACTRIS DMP                                            | 1                            |
| data_sublevel             | optional                    | float     | More detailed definition of data level, e.g. 1.5 for EBAS NRT data                          | 1.5                          |
| data_product              | mandatory                     | string    | Fixed list of data products                                                                 | "quality assured data"                |
