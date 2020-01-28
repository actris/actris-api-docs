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
* [md_distribution_information](#distribution-information)
* [dq_data_quality_information](#data-quality-information)
* [md_actris_specific](#other)

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

| Metadata Element Name | Metadata Element REST API syntax | Data type | Description                                                                          | Example                           |
|-----------------------|----------------------------------|-----------|--------------------------------------------------------------------------------------|-----------------------------------|
| keyword               | keyword                          | string    | keyword(s) describing the theme of the dataset, preferably from the WMO keyword list | Aerosol, Atmospheric, Measurement |

## md_data_identification

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

## ex_geographic_bounding_box

| Metadata element name | Metadata element REST API syntax | Data type | Description                                                                                                                            | Example |
|-----------------------|----------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|---------|
| westBoundLongitude    | west_bound_longitude             | decimal   | western-most coordinate of the limit of the dataset extent (bounding box), expressed in longitude in decimal degrees (positve east)    | +3.12   |
| eastBoundLongitude    | east_bound_longitude             | decimal   | eastern-most coordinate of the limit of the dataset extent (bounding box), expressed in longitude in decimal degrees (positve east)    | +3.13   |
| southBoundLatitude    | south_bound_latitude             | decimal   | southern-most coordinate of the limit of the dataset extent (bounding box), expressed in longitude in decimal degrees (positve northt) | +42.25  |
| northBoundLatitude    | north_bound_latitude             | decimal   | northern-most coordinate of the limit of the dataset extent (bounding box), expressed in longitude in decimal degrees (positve north)  | +42.26  |

## ex_temporal_extent
	
| Metadata element name | Metadata element REST API syntax | Data type | Description        | Example             |
|-----------------------|----------------------------------|-----------|--------------------|---------------------|
| TimePeriodBegin       | time_period_begin                | date      | dataset start time | yyyy-mm-ddThh-mm-ss |
| TimePeriodEnd         | time_period_end                  | date      | dataset end time   | yyyy-mm-ddThh-mm-ss |

## ex_vertical_extent

| Metadata element name | Metadata element REST API syntax | Data type | Description                                                                  | Example                       |
|-----------------------|----------------------------------|-----------|------------------------------------------------------------------------------|-------------------------------|
| minimumValue          | minimum_value                    | Real      | lowest vertical extent contained in the dataset (altitude of the instrument) | station altitude + height agl |
| maximumValue          | maximum_value                    | Real      | highest vertical extent contained in the dataset (reach of instrument)       | station altitude + height agl |
| unitOfMeasure         | unit_of_measure                  | String    | unit of measure (→WIS requires "m above sea level")                          | m above sea level             |

## md_content_information

| Metadata element name | Metadata element REST API syntax | Data type      | Description                                                                   | Example             |
|-----------------------|----------------------------------|----------------|-------------------------------------------------------------------------------|---------------------|
| attributeDescription  | attribute_description            | string         | parameter name                                                                | air_temperature     |
| contentType           | content_type                     | CodeList B5.12 | type of information represented by the cell value (select from dropdown list) | physicalMeasurement |


## md_distribution_information

| Metadata element name  | Metadata element REST API syntax | Data type      | Description                                                                                                                                       | Example                                                                                                                                                                                                                       |
|------------------------|----------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name                   | data_format                      | String         | name of the data transfer format                                                                                                                  | netCDF                                                                                                                                                                                                                        |
| version                | version_data_format              | String         | version of the format (data, number, etc)                                                                                                         | 4                                                                                                                                                                                                                             |
| transferSize           | transfersize                     | Real           | estimated size of a unit in the specified transfer format, expressed in megabytes. The transfersize is > 0.0                                      | 0.3                                                                                                                                                                                                                           |
| linkage                | dataset_url                      | URL            | location (address) for on-line access using Uniform Resource Locator address or similar addressing scheme such as http://www.statkart.no/isotc211 | https://thredds.nilu.no/thredds/fileServer/ebas/NO0042G.20171229200000.20190430232636.dmps.particle_number_size_distribution.pm10_non_volatile.16mo.1h.NO01L_DMPS_ZEP1_NRT.NO01L_dmps_DMPS_ZEP02_nonvol__lev0-proc-v0-2-0..nc |
| protocol               | protocol                         | String         | connection protocol to be used                                                                                                                    | http                                                                                                                                                                                                                          |
| description            | description                      | String         | detailed text description of what the online resource is/does                                                                                     | Direct download of data file (netCDF)                                                                                                                                                                                         |
| function               | function                         | CodeList B.5.3 | code for function performed by the online resource                                                                                                | download                                                                                                                                                                                                                      |

### restriction
| Metadata element name  | Metadata element REST API syntax | Data type      | Description                                                                                                                                       | Example                                                                                                                                                                                                                       |
|------------------------|----------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| set           | is_restricted                    | bool           | If authentication is required, True/False                                                                                                         | True                                                                                                                                                                                                                          |
| description_url | restriction_description          | string         | Information on how to get access                                                                                                                  | Go to somepage.com/create_user                                                                                                                                                                                                |

## dq_data_quality_information

| Metadata element name | Metadata element REST API syntax | Data type       | Description                                                                                     | Example                                                                                                                                                      |
|-----------------------|----------------------------------|-----------------|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| level                 | level                            | CodeList B.5.25 | scope to which the metadata applies:                                                            | dataset                                                                                                                                                      |
| statement             | statement                        | string          | (→WIS requires "dataset" or "series", where "series" describes a collection of single datasets) | Data collected according to instrument specific standard operating procedures, checked on import into data base.                                             |
| description           | description                      | string          | general explanation of the data producer's knowledge about the lineage of a dataset             | Regularly calibrated by instrument operator, manually quality assured by instrument operator, boundary checked by data centre, outlier check by data centre. |

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
