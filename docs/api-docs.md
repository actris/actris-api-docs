# ACTRIS metadata catalog REST API

## Add metadata record

### URL

```sh
> POST https://dev-actris-md.nilu.no/metadata/add
```

### Parameters

#### md_metadata



| Parameter | Required | Data type | Description                                                                                                   | Example                                                              |
|-----------------------|----------------------------------|-----------|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| fileIdentifier        | mandatory                  | string    | Unique identifier for this metadata file, following internal file naming convention                             | Mission.Sensor.Level.Specie.geoID.ProcessinLevel.Version.yyyymmdd.nc |
| language              | mandatory                         | string    | language used for documenting metadata (WIS requires english ""en"")                                            | en                                                                   |
| characterSet          | mandatory                    | string    | Full name of the character coding standard used for the metadata set                                            | utf8                                                                 |
| hierarchyLevel        | mandatory                  | string    | scope to which the metadata applies: "dataset"" or ""series"", where ""series"" describes a collection datasets | dataset                                                              |
| datestamp             | mandatory                        | date      | date that the metadata was created                                                                              | 2012-05-20T09:45:00                                                  |

##### Contact

| Parameter | Required | Data Type | Description                                                                                                      | Example                                                                                                       |
|-----------------------|----------------------------------|-----------|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| first_name        | mandatory                   | string    | name of the responsible person within WDC host organisation: surname, given name, title separated by a delimiter | Markus.                                                                                           |
| last_name        | mandatory                   | string    | name of the responsible person within WDC host organisation: surname, given name, title separated by a delimiter | Fiebig                                                                                         |
| organisation_name      | mandatory                 | string    | name of WDC host organisation                                                                                    | Norwegian Institute for Air Research                                                                          |
| position_name          | optional                    | string    | role or position of the responsible person within WDC host organisation (function, division)                     | Senior Scientist, Dept. Atmospheric and Climate Research (ATMOS), Norwegian Institute for Air Research (NILU) |
| role_code              | mandatory                        | string    | function performed by the WDC host organisation (select from dropdown list)                                      | custodian                                                                                                     |
| delivery_point         | optional                   | string    | street name and number                                                                                           | Instituttveien 18                                                                                             |
| address_city           | optional                     | string    | city                                                                                                             | Kjeller                                                                                                       |
| administrative_area    | optional             | string    | state, province                                                                                                  | Viken                                                                                                         |
| postal_code            | optional                      | string    | ZIP or other postal code                                                                                         | 2007                                                                                                          |
| country               | mandatory                          | string    | country                                                                                                          | Norway                                                                                                        |
| email | optional                            | string    | email address of the responsible organization or individual                                                      | some.name@email.com                                                                                           |

##### Online Resource

| Parameter | Required | Data Type | Description                    | Example              |
|-----------------------|----------------------------------|-----------|--------------------------------|----------------------|
| linkage               | mandatory                          | URL       | web address of the data center | http://ebas.nilu.no/ |


##### md_identification

Metadata related to the dataset.

| Parameter | Required | Data type      | Description                                                                                                    | Example                                                                                                                                                                                           |
|-----------------------|----------------------------------|----------------|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract              | mandatory                         | string         | short description of the dataset described (abstract)(e.g.: parameter, method, instrument, interval, site etc) | Ground based in situ observations of particle_number_size_distribution at Zeppelin mountain (Ny-Ålesund) (NO0042G) using dmps. Parameters measured are: particle_number_size_distribution in pm1. |
| title                 | mandatory                            | string         | name by which the cited reference is known                                                                     | EBAS.<station code>.<start date / time>.<revision date / time>.<component>.<matrix>.<period code>.<resolution code>.<data level>                                                                  |
| identifier            | optional                       | string         | value uniquely identifying an object within a namespace. DOI of the dataset, if available                      | https://doi.org/10.21336/gen.2                                                                                                                                                                    |
| date                  | mandatory                             | date           | reference date of the dataset                                                                                  | yyyy-mm-ddThh-mm-ss                                                                                                                                                                               |
| dateType              | mandatory                        | CodeList B.5.2 | event used for reference date                                                                                  | revision                                                                                                                                                                                          |

##### Contact

| Parameter | Required | Data Type | Description                                                                                                      | Example                                                                                                       |
|-----------------------|----------------------------------|-----------|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| first_name        | mandatory                   | string    | name of the responsible person within WDC host organisation: surname, given name, title separated by a delimiter | Markus.                                                                                           |
| last_name        | mandatory                   | string    | name of the responsible person within WDC host organisation: surname, given name, title separated by a delimiter | Fiebig                                                                                         |
| organisation_name      | mandatory                 | string    | name of WDC host organisation                                                                                    | Norwegian Institute for Air Research                                                                          |
| position_name          | optional                    | string    | role or position of the responsible person within WDC host organisation (function, division)                     | Senior Scientist, Dept. Atmospheric and Climate Research (ATMOS), Norwegian Institute for Air Research (NILU) |
| role_code              | mandatory                        | string    | function performed by the WDC host organisation (select from dropdown list)                                      | custodian                                                                                                     |
| delivery_point         | optional                   | string    | street name and number                                                                                           | Instituttveien 18                                                                                             |
| address_city           | optional                     | string    | city                                                                                                             | Kjeller                                                                                                       |
| administrative_area    | optional             | string    | state, province                                                                                                  | Viken                                                                                                         |
| postal_code            | optional                      | string    | ZIP or other postal code                                                                                         | 2007                                                                                                          |
| country               | mandatory                          | string    | country                                                                                                          | Norway                                                                                                        |
| email | optional                            | string    | email address of the responsible organization or individual                                                      | some.name@email.com                                                                                           |

##### Online Resource

| Parameter | Required | Data Type | Description                    | Example              |
|-----------------------|----------------------------------|-----------|--------------------------------|----------------------|
| linkage               | mandatory                         | URL       | web address of the data center | http://ebas.nilu.no/ |

#### md_constraints

| Parameter | Required | Data type | Description                                                                                 | Example                                     |
|-----------------------|----------------------------------|-----------|---------------------------------------------------------------------------------------------|---------------------------------------------|
| access_constraints     | mandatory                  | string    | access constraints of the published data                                                    | otherRestrictions                           |
| use_constraints        | mandatory                  | string    | any special restrictions or limitations or warnings on using the data                       | otherRestrictions                           |
| other_constraints      | mandatory                           | string    | other restrictions and legal prerequisites for accessing and using the resource or metadata | https://www.gaw-wdca.org/Browse-Obtain-Data |
| data_licence           | optional                     | string    | fixed list of available licences                                                            | CC-BY 4.0                               |
| metadata_licence       | optional                 | string    | fixed list of available licences                                                            | CC0                               |

#### md_keywords

| Parameter | Required | Data type | Description                                                                          | Example                           |
|-----------------------|----------------------------------|-----------|--------------------------------------------------------------------------------------|-----------------------------------|
| keyword               | mandatory                          | string    | keyword(s) describing the theme of the dataset, preferably from the WMO keyword list | ["NO0042G,", "Zeppelin", "mountain", "(Ny-\u00c5lesund),", "pm10,", "particle_number_size_distribution,", "GAW-WDCA,", "ACTRIS,", "EMEP,", "NILU"] |

#### md_data_identification

| Parameter | Required | Data type       | Description                                                     | Example                                      |
|-----------------------|----------------------------------|-----------------|-----------------------------------------------------------------|----------------------------------------------|
| language              | mandatory                         | string          | language used within the dataset                                | en                                           |
| characterSet          | mandatory                    | CodeList B.5.10 | full name of the character coding standard used for the dataset | utf8                                         |
| topicCategory         | mandatory                   | CodeList B.5.27 | main theme(s) of the dataset                                    | climatologyMeteorologyAtmosphere             |
| description           | mandatory                      | string          | description of spatial and temporal extent for the dataset      | time series of point measurements at surface |
| code                  | mandatory               | string          | Station WMO region                                              | VI - Europe                                  |
| code                  | mandatory                     | string          | country the measurement site is located in (in english)         | Norway                                       |
| code                  | mandatory                     | string          | Name of station, platform or observatory                        | Birkenes                                     |
| code                  | mandatory               | string          | Identifier of station/observatory based on GAW-ID               | BIR                                          |

#### ex_geographic_bounding_box

| Parameter | Required | Data type | Description                                                                                                                            | Example |
|-----------------------|----------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|---------|
| west_bound_longitude    | mandatory             | decimal   | western-most coordinate of the limit of the dataset extent (bounding box), expressed in longitude in decimal degrees (positve east)    | 11.88934   |
| east_bound_longitude    | mandatory             | decimal   | eastern-most coordinate of the limit of the dataset extent (bounding box), expressed in longitude in decimal degrees (positve east)    | 11.88934   |
| south_bound_latitude    | mandatory             | decimal   | southern-most coordinate of the limit of the dataset extent (bounding box), expressed in longitude in decimal degrees (positve northt) | 78.90669  |
| north_bound_latitude    | mandatory             | decimal   | northern-most coordinate of the limit of the dataset extent (bounding box), expressed in longitude in decimal degrees (positve north)  | 78.90669  |

#### ex_temporal_extent
	
| Parameter | Required | Data type | Description        | Example             |
|-----------------------|----------------------------------|-----------|--------------------|---------------------|
| time_period_begin       | mandatory                | date      | dataset start time (ISO 8601) | "2018-01-01T00:00:00" |
| time_period_end         | mandatory                  | date      | dataset end time (ISO 8601)  | 2019-01-01T00:00:00 |

#### ex_vertical_extent

| Parameter | Required | Data type | Description                                                                  | Example                       |
|-----------------------|----------------------------------|-----------|------------------------------------------------------------------------------|-------------------------------|
| minimum_value          | optional                    | Real      | lowest vertical extent contained in the dataset (altitude of the instrument) | null |
| maximum_value          | optional                    | Real      | highest vertical extent contained in the dataset (reach of instrument)       | 475.0 |
| unit_of_measure         | optional                  | String    | unit of measure (→WIS requires "m above sea level")                          | "m above sea level"             |

#### md_content_information

| Parameter | Required | Data type      | Description                                                                   | Example             |
|-----------------------|----------------------------------|----------------|-------------------------------------------------------------------------------|---------------------|
| attribute_description  | mandatory            | string         | parameter name                                                                | ["particle_number_size_distribution"]     |
| content_type           | mandatory                     | CodeList B5.12 | type of information represented by the cell value (select from dropdown list) | "physicalMeasurement" |


#### md_distribution_information

| Parameter  | Required | Data type      | Description                                                                                                                                       | Example                                                                                                                                                                                                                       |
|------------------------|----------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| data_format            | mandatory                      | String         | name of the data transfer format                                                                                                                  | netCDF                                                                                                                                                                                                                        |
| version_data_format    | mandatory              | String         | version of the format (data, number, etc)                                                                                                         | 4                                                                                                                                                                                                                             |
| transfersize           | optional                    | Real           | estimated size of a unit in the specified transfer format, expressed in megabytes. The transfersize is > 0.0                                      | 0.3                                                                                                                                                                                                                           |
| dataset_url            | mandatory                      | URL            | location (address) for on-line access using Uniform Resource Locator address or similar addressing scheme such as http://www.statkart.no/isotc211 | https://thredds.nilu.no/thredds/fileServer/ebas/NO0042G.20171229200000.20190430232636.dmps.particle_number_size_distribution.pm10_non_volatile.16mo.1h.NO01L_DMPS_ZEP1_NRT.NO01L_dmps_DMPS_ZEP02_nonvol__lev0-proc-v0-2-0..nc |
| protocol               | mandatory                        | String         | connection protocol to be used                                                                                                                    | http                                                                                                                                                                                                                          |
| description            | optional                     | String         | detailed text description of what the online resource is/does                                                                                     | Direct download of data file (netCDF)                                                                                                                                                                                         |
| function               | mandatory                         | CodeList B.5.3 | code for function performed by the online resource                                                                                                | download                                                                                                                                                                                                                      |

##### restriction
| Parameter  | Required | Data type      | Description                                                                                                                                       | Example                                                                                                                                                                                                                       |
|------------------------|----------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| set           | mandatory                    | bool           | If authentication is required, True/False                                                                                                         | true                                                                                                                                                                                                                          |
| description_url | optional          | string         | Information on how to get access                                                                                                                  | "https://somepage.com/create_user"                                                                                                                                                                                                |

#### dq_data_quality_information

| Parameter | Required | Data type       | Description                                                                                     | Example                                                                                                                                                      |
|-----------------------|----------------------------------|-----------------|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| level                 | optional                            | CodeList B.5.25 | scope to which the metadata applies:                                                            | dataset                                                                                                                                                      |
| statement             | optional                        | string          | (→WIS requires "dataset" or "series", where "series" describes a collection of single datasets) | Data collected according to instrument specific standard operating procedures, checked on import into data base.                                             |
| description           | optional                      | string          | general explanation of the data producer's knowledge about the lineage of a dataset             | Regularly calibrated by instrument operator, manually quality assured by instrument operator, boundary checked by data centre, outlier check by data centre. |

#### md_actris_specific

| Parameter    | Required | Data type | Description                                                                                 | Example                      |
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

### Response

```js
{
	"Server": "nginx/1.10.3 (Ubuntu)",
	"Date": "Fri, 31 Jan 2020 08:12:24 GMT",
	"Content-Length": "0",
	"Connection": "keep-alive",
	"Location": "http://dev-actris-md.nilu.no/Metadata/398",
	"Strict-Transport-Security": "max-age=31536; includeSubDomains"
}
```

### Errors

- **500** - Internal Server Error
- **400** - Bad Request

## Get metadata record by id

### URL

```sh
> GET https://dev-actris-md.nilu.no/Metadata/398
```

### Response

```js
[{
	"md_metadata": {
		"id": 398,
		"file_identifier": "NO0042G.20180101000000.20190508191242.dmps.particle_number_size_distribution.pm10.1y.1h.NO01L_NILU_DMPSmodel2_ZEP.NO01L_dmps_DMPS_ZEP01.lev2.nc",
		"language": "en",
		"hierarchy_level": "dataset",
		"online_resource": {
			"linkage": "https://www.nilu.no/"
		},
		"datestamp": "2019-05-08T17:12:42.0000000Z",
		"created": "2020-01-31T08:12:25.0000000Z",
		"contact": [{
			"first_name": "Markus",
			"last_name": "Fiebig",
			"organisation_name": "Norwegian Institute for Air Research (NILU)",
			"role_code": ["custodian"],
			"country": "Norway",
			"delivery_point": "Insituttveien 18",
			"address_city": "Kjeller",
			"administrative_area": "Viken",
			"postal_code": 2007,
			"email": "ebas@nilu.no",
			"position_name": "Senior Scientist"
		}]
	},
	"md_identification": {
		"abstract": "Ground based in situ observations of particle_number_size_distribution at Zeppelin mountain (Ny-Ålesund) (NO0042G) using dmps. These measurements are gathered as a part of the following projects ACTRIS, EMEP, NILU, GAW-WDCA and they are stored in the EBAS database (http://ebas.nilu.no/). Parameters measured are: particle_number_size_distribution in pm10",
		"title": "Ground based in situ observations of particle_number_size_distribution at Zeppelin mountain (Ny-Ålesund) (NO0042G) using dmps",
		"date_type": "creation",
		"contact": [{
			"first_name": "Markus",
			"last_name": "Fiebig",
			"organisation_name": "\"Norwegian Institute for Air Research",
			"role_code": ["principalInvestigator"],
			"country": "Norway",
			"delivery_point": null,
			"address_city": null,
			"administrative_area": null,
			"postal_code": null,
			"email": "Markus.Fiebig@nilu.no",
			"position_name": null
		}, {
			"first_name": "Chris",
			"last_name": "Lunder",
			"organisation_name": " Atmosphere and Climate Department",
			"role_code": ["principalInvestigator"],
			"country": "Norway",
			"delivery_point": null,
			"address_city": null,
			"administrative_area": null,
			"postal_code": null,
			"email": " crl@nilu.no",
			"position_name": null
		}],
		"online_resource": {
			"linkage": "http://ebas.nilu.no/"
		},
		"identifier": "https://doi.org/10.21336/some.doi.1",
		"date": "2019-05-08T17:12:42.0000000Z"
	},
	"md_constraints": {
		"access_constraints": "otherRestrictions",
		"use_constraints": "otherRestrictions",
		"other_constraints": "ACTRIS: http://actris.nilu.no/Content/Documents/DataPolicy.pdf, EMEP: Public open access. We encourage contacting data originators if substatial use of individual time series is planned (fair use data policy)., NILU: Public open access. We encourage contacting data originators if substatial use of individual time series is planned (fair use data policy)., GAW-WDCA: "
	},
	"md_keywords": {
		"keywords": ["(Ny-Ålesund),", "ACTRIS,", "EMEP,", "GAW-WDCA,", "mountain", "NILU", "NO0042G,", "particle_number_size_distribution,", "pm10,", "Zeppelin"]
	},
	"md_data_identification": {
		"language": "en",
		"topic_category": "climatologyMeteorologyAtmosphere",
		"description": "time series of point measurements at surface",
		"station_wmo_region": "6",
		"country_name": "Norway",
		"station_name": "Zeppelin Mountain (Ny Ålesund)",
		"station_identifier": "ZEP"
	},
	"ex_geographic_bounding_box": {
		"west_bound_longitude": 11.88934,
		"east_bound_longitude": 11.88934,
		"south_bound_latitude": 78.90669,
		"north_bound_latitude": 78.90669
	},
	"ex_temporal_extent": {
		"time_period_begin": "2017-12-31T23:00:00.0000000Z",
		"time_period_end": "2018-12-31T23:00:00.0000000Z"
	},
	"ex_vertical_extent": {
		"minimum_value": null,
		"maximum_value": null,
		"unit_of_measure": "m above sea level"
	},
	"md_content_information": {
		"attribute_description": ["particle_number_size_distribution"],
		"content_type": "physicalMeasurement"
	},
	"md_distribution_information": {
		"data_format": "NETCDF3_CLASSIC",
		"version_data_format": "NETCDF3_CLASSIC",
		"dataset_url": "https://thredds.nilu.no/thredds/dodsC/ebas/NO0042G.20180101000000.20190508191242.dmps.particle_number_size_distribution.pm10.1y.1h.NO01L_NILU_DMPSmodel2_ZEP.NO01L_dmps_DMPS_ZEP01.lev2.nc",
		"protocol": "HTTP",
		"function": "download",
		"restriction": {
			"set": false,
			"description_url": "https://ebas-submit.nilu.no/Data-Policy"
		},
		"transfersize": null,
		"description": "Direct download of data file"
	},
	"md_actris_specific": {
		"platform_type": "surface_station",
		"product_type": "observation",
		"matrix": "particle",
		"sub_matrix": "pm10",
		"instrument_type": ["dmps"],
		"program_affiliation": ["ACTRIS"],
		"legacy_data": false,
		"data_level": 2,
		"data_product": "quality assured data",
		"data_sublevel": null
	},
	"dq_data_quality_information": {
		"level": "dataset",
		"statement": "Data collected according to instrument specific standard operating procedures, checked on import into data base.",
		"description": "processing_level_test"
	}
}]
```

### Errors

## Get all metadata records

### URL

```sh
> GET https://dev-actris-md.nilu.no/Metadata
```

### Response

```js
[{
	"md_metadata": {
		"id": 214,
		"file_identifier": "EBAS240209145",
		"language": "en",
		"hierarchy_level": "dataset",
		"online_resource": {
			"linkage": "https://www.nilu.no/"
		},
		"datestamp": "2012-05-20T07:45:00.0000000Z",
		"created": "2020-01-16T23:00:00.0000000Z",
		"contact": [{
			"first_name": "Markus",
			"last_name": "Fiebig",
			"organisation_name": "Norwegian Institute for Air Research",
			"role_code": ["custodian", "originator", "processor"],
			"country": "Norway",
			"delivery_point": "Insituttveien 18",
			"address_city": "Kjeller",
			"administrative_area": "Viken",
			"postal_code": 2007,
			"email": "some.name@email.com",
			"position_name": "Senior Scientist"
		}]
	},
	"md_identification": {
		"abstract": "Ground based in situ observations of particle_number_size_distribution at Zeppelin mountain (Ny-Ålesund) (NO0042G) using dmps. Parameters measured are: particle_number_size_distribution in pm1.",
		"title": "Ground based in situ observations of particle_number_size_distribution at Zeppelin mountain (Ny-Ålesund) (NO0042G) using dmps",
		"date_type": "revision",
		"contact": [{
			"first_name": "Markus",
			"last_name": "Fiebig",
			"organisation_name": "Norwegian Institute for Air Research",
			"role_code": ["custodian", "originator", "processor"],
			"country": "Norway",
			"delivery_point": "Insituttveien 18",
			"address_city": "Kjeller",
			"administrative_area": "Viken",
			"postal_code": 2007,
			"email": "some.name@email.com",
			"position_name": "Senior Scientist"
		}],
		"online_resource": {
			"linkage": "http://ebas.nilu.no/"
		},
		"identifier": null,
		"date": "2012-05-20T07:45:00.0000000Z"
	},
	"md_constraints": {
		"access_constraints": "otherRestrictions",
		"use_constraints": "otherRestrictions",
		"other_constraints": "ACTRIS: http://actris.nilu.no/Content/Documents/DataPolicy.pdf, EMEP: Public open access. We encourage contacting data originators if substatial use of individual time series is planned (fair use data policy)., NILU: Public open access. We encourage contacting data originators if substatial use of individual time series is planned (fair use data policy)., GAW-WDCA:",
		"data_licence": "CC-BY 4.0",
		"metadata_licence": "CC0"
	},
	"md_keywords": {
		"keywords": ["ACTRIS", "EMEP", "GAW-WDCA", "NILU", "NO0042G", "particle_number_size_distribution", "pm10", "Zeppelin mountain (Ny-Ålesund)"]
	},
	"md_data_identification": {
		"language": "en",
		"topic_category": "climatologyMeteorologyAtmosphere",
		"description": "time series of point measurements at surface",
		"station_wmo_region": "VI - Europe",
		"country_name": "Norway",
		"station_name": "Birkenes",
		"station_identifier": "BIR"
	},
	"ex_geographic_bounding_box": {
		"west_bound_longitude": 3.12,
		"east_bound_longitude": 3.13,
		"south_bound_latitude": 42.25,
		"north_bound_latitude": 42.26
	},
	"ex_temporal_extent": {
		"time_period_begin": "2019-11-20T07:45:17.0000000Z",
		"time_period_end": "2019-11-20T09:45:17.0000000Z"
	},
	"ex_vertical_extent": {
		"minimum_value": 24.5,
		"maximum_value": 200.0,
		"unit_of_measure": "m above sea level"
	},
	"md_content_information": {
		"attribute_description": ["backscatter", "particle_extinction"],
		"content_type": "physicalMeasurement"
	},
	"md_distribution_information": {
		"data_format": "netcdf",
		"version_data_format": "4",
		"dataset_url": "https://thredds.nilu.no/thredds/fileServer/ebas/NO0042G.20180101000000.20190508191242.dmps.particle_number_size_distribution.pm10.1y.1h.NO01L_NILU_DMPSmodel2_ZEP.NO01L_dmps_DMPS_ZEP01.lev2.nc",
		"protocol": "HTTP",
		"function": "download",
		"restriction": {
			"set": false,
			"description_url": "http://Go to somepage.com/create_user"
		},
		"transfersize": null,
		"description": null
	},
	"md_actris_specific": {
		"platform_type": "surface_station",
		"product_type": "observation",
		"matrix": "particle",
		"sub_matrix": "pm10",
		"instrument_type": ["dmps"],
		"program_affiliation": ["EMEP"],
		"legacy_data": false,
		"data_level": 1,
		"data_product": "Higher level data product",
		"data_sublevel": 1.5
	},
	"dq_data_quality_information": {
		"level": "dataset",
		"statement": null,
		"description": null
	}
}, {
	"md_metadata": {
		"id": 215,
		"file_identifier": "EBAS24020914123",
		"language": "en",
		"hierarchy_level": "dataset",
		"online_resource": {
			"linkage": "https://www.nilu.no/"
		},
		"datestamp": "2019-11-20T07:45:17.0000000Z",
		"created": "2020-01-16T23:00:00.0000000Z",
		"contact": [{
			"first_name": "Richard",
			"last_name": "Rud",
			"organisation_name": "Norwegian Institute for Air Research",
			"role_code": ["custodian"],
			"country": "Norway",
			"delivery_point": "Insituttveien 18",
			"address_city": "Kjeller",
			"administrative_area": "Viken",
			"postal_code": 2007,
			"email": "some.name@email.com",
			"position_name": "Senior Scientist"
		}]
	},
	"md_identification": {
		"abstract": "Ground based in situ observations of particle_number_size_distribution at Zeppelin mountain (Ny-Ålesund) (NO0042G) using dmps. Parameters measured are: particle_number_size_distribution in pm1.",
		"title": "Ground based in situ observations of particle_number_size_distribution at Zeppelin mountain (Ny-Ålesund) (NO0042G) using dmps",
		"date_type": "revision",
		"contact": [{
			"first_name": "Markus",
			"last_name": "Fiebig",
			"organisation_name": "Norwegian Institute for Air Research",
			"role_code": ["custodian", "originator", "processor"],
			"country": "Norway",
			"delivery_point": "Insituttveien 18",
			"address_city": "Kjeller",
			"administrative_area": "Viken",
			"postal_code": 2007,
			"email": "some.name@email.com",
			"position_name": "Senior Scientist"
		}],
		"online_resource": {
			"linkage": "http://ebas.nilu.no/"
		},
		"identifier": "https://doi.org/10.21336/some.doi.1",
		"date": "2019-11-20T08:45:17.0000000Z"
	},
	"md_constraints": {
		"access_constraints": "otherRestrictions",
		"use_constraints": "otherRestrictions",
		"other_constraints": "ACTRIS: http://actris.nilu.no/Content/Documents/DataPolicy.pdf, EMEP: Public open access. We encourage contacting data originators if substatial use of individual time series is planned (fair use data policy)., NILU: Public open access. We encourage contacting data originators if substatial use of individual time series is planned (fair use data policy)., GAW-WDCA:",
		"data_licence": "CC-BY 4.0",
		"metadata_licence": "CC0"
	},
	"md_keywords": {
		"keywords": ["ACTRIS", "EMEP", "GAW-WDCA", "NILU", "NO0042G", "particle_number_size_distribution", "pm10", "Zeppelin mountain (Ny-Ålesund)"]
	},
	"md_data_identification": {
		"language": "en",
		"topic_category": "climatologyMeteorologyAtmosphere",
		"description": "time series of point measurements at surface",
		"station_wmo_region": "VI - Europe",
		"country_name": "Norway",
		"station_name": "Birkenes",
		"station_identifier": "BIR"
	},
	"ex_geographic_bounding_box": {
		"west_bound_longitude": 3.12,
		"east_bound_longitude": 3.12,
		"south_bound_latitude": 42.25,
		"north_bound_latitude": 42.25
	},
	"ex_temporal_extent": {
		"time_period_begin": "2019-11-20T07:45:17.0000000Z",
		"time_period_end": "2019-11-20T09:45:17.0000000Z"
	},
	"ex_vertical_extent": {
		"minimum_value": 24.5,
		"maximum_value": 200.0,
		"unit_of_measure": "m above sea level"
	},
	"md_content_information": {
		"attribute_description": ["backscatter", "particle_extinction"],
		"content_type": "physicalMeasurement"
	},
	"md_distribution_information": {
		"data_format": "netcdf",
		"version_data_format": "4",
		"dataset_url": "https://thredds.nilu.no/thredds/fileServer/ebas/NO0042G.20180101000000.20190508191242.dmps.particle_number_size_distribution.pm10.1y.1h.NO01L_NILU_DMPSmodel2_ZEP.NO01L_dmps_DMPS_ZEP01.lev2.nc",
		"protocol": "HTTP",
		"function": "download",
		"restriction": {
			"set": false,
			"description_url": "http://somepage.com/create_user"
		},
		"transfersize": 0.5,
		"description": "Direct download of data file"
	},
	"md_actris_specific": {
		"platform_type": "surface_station",
		"product_type": "observation",
		"matrix": "particle",
		"sub_matrix": "pm10",
		"instrument_type": ["dmps"],
		"program_affiliation": ["EMEP", "GAW-WDCA"],
		"legacy_data": false,
		"data_level": 1,
		"data_product": "Higher level data product",
		"data_sublevel": 1.5
	},
	"dq_data_quality_information": {
		"level": "dataset",
		"statement": "Data collected according to instrument specific standard operating procedures, checked on import into data base.",
		"description": "Regularly calibrated by instrument operator, manually quality assured by instrument operator, boundary checked by data centre, outlier check by data centre."
	}
}, {
	"md_metadata": {
		"id": 216,
		"file_identifier": "EBAS24020914123",
		"language": "en",
		"hierarchy_level": "dataset",
		"online_resource": {
			"linkage": "https://www.nilu.no/"
		},
		"datestamp": "2019-11-20T07:45:17.0000000Z",
		"created": "2020-01-16T23:00:00.0000000Z",
		"contact": [{
			"first_name": "Richard",
			"last_name": "Rud",
			"organisation_name": "Norwegian Institute for Air Research",
			"role_code": ["custodian"],
			"country": "Norway",
			"delivery_point": "Insituttveien 18",
			"address_city": "Kjeller",
			"administrative_area": "Viken",
			"postal_code": 2007,
			"email": "some.name@email.com",
			"position_name": "Senior Scientist"
		}]
	},
	"md_identification": {
		"abstract": "Ground based in situ observations of particle_number_size_distribution at Zeppelin mountain (Ny-Ålesund) (NO0042G) using dmps. Parameters measured are: particle_number_size_distribution in pm1.",
		"title": "Ground based in situ observations of particle_number_size_distribution at Zeppelin mountain (Ny-Ålesund) (NO0042G) using dmps",
		"date_type": "revision",
		"contact": [{
			"first_name": "Markus",
			"last_name": "Fiebig",
			"organisation_name": "Norwegian Institute for Air Research",
			"role_code": ["custodian", "originator", "processor"],
			"country": "Norway",
			"delivery_point": "Insituttveien 18",
			"address_city": "Kjeller",
			"administrative_area": "Viken",
			"postal_code": 2007,
			"email": "some.name@email.com",
			"position_name": "Senior Scientist"
		}],
		"online_resource": {
			"linkage": "http://ebas.nilu.no/"
		},
		"identifier": "https://doi.org/10.21336/some.doi.1",
		"date": "2019-11-20T08:45:17.0000000Z"
	},
	"md_constraints": {
		"access_constraints": "otherRestrictions",
		"use_constraints": "otherRestrictions",
		"other_constraints": "ACTRIS: http://actris.nilu.no/Content/Documents/DataPolicy.pdf, EMEP: Public open access. We encourage contacting data originators if substatial use of individual time series is planned (fair use data policy)., NILU: Public open access. We encourage contacting data originators if substatial use of individual time series is planned (fair use data policy)., GAW-WDCA:",
		"data_licence": "CC-BY 4.0",
		"metadata_licence": "CC0"
	},
	"md_keywords": {
		"keywords": ["ACTRIS", "EMEP", "GAW-WDCA", "NILU", "NO0042G", "particle_number_size_distribution", "pm10", "Zeppelin mountain (Ny-Ålesund)"]
	},
	"md_data_identification": {
		"language": "en",
		"topic_category": "climatologyMeteorologyAtmosphere",
		"description": "time series of point measurements at surface",
		"station_wmo_region": "VI - Europe",
		"country_name": "Norway",
		"station_name": "Birkenes",
		"station_identifier": "BIR"
	},
	"ex_geographic_bounding_box": {
		"west_bound_longitude": 3.12,
		"east_bound_longitude": 3.12,
		"south_bound_latitude": 42.25,
		"north_bound_latitude": 42.25
	},
	"ex_temporal_extent": {
		"time_period_begin": "2019-11-20T07:45:17.0000000Z",
		"time_period_end": "2019-11-20T09:45:17.0000000Z"
	},
	"ex_vertical_extent": {
		"minimum_value": 24.5,
		"maximum_value": 200.0,
		"unit_of_measure": "m above sea level"
	},
	"md_content_information": {
		"attribute_description": ["backscatter", "particle_extinction"],
		"content_type": "physicalMeasurement"
	},
	"md_distribution_information": {
		"data_format": "netcdf",
		"version_data_format": "4",
		"dataset_url": "https://thredds.nilu.no/thredds/fileServer/ebas/NO0042G.20180101000000.20190508191242.dmps.particle_number_size_distribution.pm10.1y.1h.NO01L_NILU_DMPSmodel2_ZEP.NO01L_dmps_DMPS_ZEP01.lev2.nc",
		"protocol": "HTTP",
		"function": "download",
		"restriction": {
			"set": false,
			"description_url": "http://somepage.com/create_user"
		},
		"transfersize": 0.5,
		"description": "Direct download of data file"
	},
	"md_actris_specific": {
		"platform_type": "surface_station",
		"product_type": "observation",
		"matrix": "particle",
		"sub_matrix": "pm10",
		"instrument_type": ["dmps"],
		"program_affiliation": ["EMEP", "GAW-WDCA"],
		"legacy_data": false,
		"data_level": 1,
		"data_product": "Higher level data product",
		"data_sublevel": 1.5
	},
	"dq_data_quality_information": {
		"level": "dataset",
		"statement": "Data collected according to instrument specific standard operating procedures, checked on import into data base.",
		"description": "Regularly calibrated by instrument operator, manually quality assured by instrument operator, boundary checked by data centre, outlier check by data centre."
	}
}

...

```

### Errors

## Get version

### URL

```sh
> GET https://dev-actris-md.nilu.no/version
```

### Response

```js
{"build":"1.0.4"}
```

### Errors
