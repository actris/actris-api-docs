# Upload file metadata

> PUT /api/files/create

**Parameters**

**file_id** (int) - file identifier *(required)*

**filename** (string) - file name *(required)*
 
**datafileurl** (string) - URL of data file *(required)*

**filesize** (string) - Size of data 

**datafilehash** (string) - hash of data file

**locationname** (string) - Station location *(required)*

**fileformat** (string) - Format of data file *(required)*

**metadataupdatedate** (date) - date of metadata update 

**filegenerationdate** (date) - date of file generation

**gmltimeperiod_gmlbeginposition** (date) - starttime *(required)*

**gmltimeperiod_gmlendposition** (date) - endtime *(required)*

**platform** (string) - Platform *(required)*

**alt** (float) - meters above sea level *(required)*

**long** (string) - longitude of station *(required)*

**lat** (string) - latitude of station *(required)*

**responsible_party** (string) - first and last name of responsible party (PI) *(required)*

**responsible_party_contact** (string) - email of responsible party *(required)*

**organisation_name** (string) - Name of research performing organization *(required)*

**doi** (string) - digital object identifier of dataset 

**licence** (string) - licence information

**fileconstraints** (string) - file constraint information

**data_policy_url** (string) - url of data policy

**description** (string) - additional field for description

**originatingdatacenter** (string) - acronym of data center unit in ACTRIS *(required)*

**dataversion** (float) - version of the data file

**producttype** (string) - product type in the data file *(required)*

**variable_name** (string) - name of observed variable *(required)*

**isrestricted** (bool) - access restriction in terms of password *(required)*

**program_affiliation** (string) - associated projects and networks

**Request: JSON Object**

**Response: JSON Object**

**file_id** (int) – file identifier

**message** (string) – HTTP status text

**http-status-code** (int) – HTTP status code

**atom** (string) – atom URL to file metadata in the API

**Status Codes:	** 500 - Internal Server Error
              error-code (int) – application error
			  400 - Bad Request
			  115 - Invalid parameter schema
			  220 - Producttype not found in system
			  410 - Filename conflict

#### Example request

> PUT /api/files/create HTTPS/1.1

> Host: https://actris-rest-api.nilu.no

> Accept: application/json

> Content-Type: application/json

```
[{
	"file_id": 1234,
	"filename": "NO0042G.20180212000000.20190614000000.high_vol_sampler..air+aerosol.10mo.4w.NO01L_fppuf_42a.NO01L_NILU.lev2.nc",
	"datafileurl": "https://thredds.nilu.no/thredds/fileServer/ebas/NO0042G.20180212000000.20190614000000.high_vol_sampler..air+aerosol.10mo.4w.NO01L_fppuf_42a.NO01L_NILU.lev2.nc",
	"filesize": "92,4 kB",
	"datafilehash": false,
	"locationname": "Zeppelin mountain (Ny-Ålesund)",
	"fileformat": "netCDF4",
	"metadataupdatedate": "2019 - 06 - 14 T00: 00: 00 UTC",
	"filegenerationdate": "2019 - 06 - 14 T00: 00: 00 UTC",
	"gml_beginposition": "2018 - 02 - 23 T12: 00: 00 Z",
	"gml_endposition": "2018 - 12 - 11 T00: 00: 00 Z",
	"platform": "groundbased",
	"alt": "474.0 m",
	"long": "011° 53 '12 East",
	"lat": "78° 54 '26 North",
	"responsible_party": "Richard Rud"
	"responsible_party_contact": "ror@nilu.no",
	"organisation_name": "Norwegian Institute for Air Research, NILU, Atmosphere and Climate Department, Instituttveien 18, 2007, Kjeller, Norway",
	"doi": "",
	"licence": "",
	"fileconstraints": "",
	"data_policy_url": "https://ebas-submit.nilu.no/Data-Policy",
	"description": "Ground based in situ observations of high_vol_sampler at Zeppelin mountain (Ny-Ålesund) (NO0042G). These measurements are gathered as a part of the following projects EMEP_preliminary, CAMP, AMAP, NILU and they are stored in the EBAS database (http://ebas.nilu.no/). Parameters measured are: FTS_6-2 in air+aerosol (mass_concentration_of_6_:_2_flourotelomer_sulfonic_acid_in_aerosol), FTS_8-2 in air+aerosol, PFBS in air+aerosol (mass_concentration_of_perfluorobutanesulfonic_acid_in_aerosol), PFDA in air+aerosol, PFDS in air+aerosol, PFDoDA in air+aerosol (mass_concentration_of_perfluorododecanoic_acid_in_aerosol), PFHpA in air+aerosol (mass_concentration_of_perfluoroheptanoic_acid_in_aerosol), PFHpS in air+aerosol, PFHxA in air+aerosol (mass_concentration_of_perfluorohexanoic_acid_in_aerosol), PFHxS in air+aerosol (mass_concentration_of_perfluorohexane_sulfonic_acid_in_aerosol), PFNA in air+aerosol (mass_concentration_of_perfluorononanoic_acid_in_aerosol), PFNS in air+aerosol, PFOA in air+aerosol (mass_concentration_of_perfluorooctanoic_acid_in_aerosol), PFPS in air+aerosol, PFTeDA in air+aerosol, PFTrDA in air+aerosol",
	"originatingdatacenter": "In-Situ",
	"dataversion": 1.0,
	"producttype": "mass_concentration_of_perfluorohexane_sulfonic_acid_in_aerosol",
	"program_affiliation": "EMEP, ACTRIS"
}]
```

#### Example response

> HTTPS/1.1 201 OK

> Content-Type: application/json

```
[{
	"file_id": 1234,
	"message": "Created",
	"http-status-code": "201",
	"atom": "https://actris-rest-api.nilu.no/files/id/1234"
}]
```

# Get list of all files

> GET /api/files

**Response: JSON Array of Objects:**

**file_id** (int) - file identifier

**filename** (string) - file name
 
**datafileurl** (string) - URL of data file

**filesize** (string) - Size of data

**datafilehash** (string) - hash of data file

**locationname** (string) - Station location

**fileformat** (string) - Format of data file

**metadataupdatedate** (date) - date of metadata update

**filegenerationdate** (date) - date of file generation

**gmltimeperiod_gmlbeginposition** (date) - starttime

**gmltimeperiod_gmlendposition** (date) - endtime

**platform** (string) - Platform

**alt** (float) - meters above sea level

**long** (string) - longitude of station

**lat** (string) - latitude of station

**responsible_party** (string) - first and last name of responsible party (PI)

**responsible_party_contact** (string) - email of responsible party

**organisation_name** (string) - Name of research performing organization

**doi** (string) - digital object identifier of dataset

**licence** (string) - licence information

**fileconstraints** (string) - file constraint information

**data_policy_url** (string) - url of data policy

**description** (string) - additional field for description

**originatingdatacenter** (string) - acronym of data center unit in ACTRIS

**dataversion** (float) - version of the data file

**producttype** (string) - product type in the data file

**variable_name** (string) - name of observed variable

**isrestricted** (bool) - access restriction in terms of password

**program_affiliation** (string) - associated projects and networks

**Status Codes:	** 500 Internal Server Error
              error-code (int) – application error

## Example request:

> GET /api/files HTTPS/1.1

> Host: https://actris-rest-api.nilu.no

> Accept: application/json

## Example response:

> HTTPS/1.1 200 OK

> Content-Type: application/json

```
[{
	"file_id": 1234,
	"filename": "NO0042G.20180212000000.20190614000000.high_vol_sampler..air+aerosol.10mo.4w.NO01L_fppuf_42a.NO01L_NILU.lev2.nc",
	"datafileurl": "https://thredds.nilu.no/thredds/fileServer/ebas/NO0042G.20180212000000.20190614000000.high_vol_sampler..air+aerosol.10mo.4w.NO01L_fppuf_42a.NO01L_NILU.lev2.nc",
	"filesize": "92,4 kB",
	"datafilehash": false,
	"locationname": "Zeppelin mountain (Ny-Ålesund)",
	"fileformat": "netCDF4",
	"metadataupdatedate": "2019 - 06 - 14 T00: 00: 00 UTC",
	"filegenerationdate": "2019 - 06 - 14 T00: 00: 00 UTC",
	"gml_beginposition": "2018 - 02 - 23 T12: 00: 00 Z",
	"gml_endposition": "2018 - 12 - 11 T00: 00: 00 Z",
	"platform": "groundbased",
	"alt": "474.0 m",
	"long": "011° 53 '12 East",
	"lat": "78° 54 '26 North",
	"responsible_party": ["Ellen Katrin Enge", "Pernilla Bohlin Nizzetto"],
	"responsible_party_contact": ["eke@nilu.no", "pbn@nilu.no"],
	"organisation_name": "Norwegian Institute for Air Research, NILU, Atmosphere and Climate Department, Instituttveien 18, 2007, Kjeller, Norway",
	"doi": false,
	"licence": false,
	"fileconstraints": false,
	"data_policy_url": "https://ebas-submit.nilu.no/Data-Policy",
	"description": "Ground based in situ observations of high_vol_sampler at Zeppelin mountain (Ny-Ålesund) (NO0042G). These measurements are gathered as a part of the following projects EMEP_preliminary, CAMP, AMAP, NILU and they are stored in the EBAS database (http://ebas.nilu.no/). Parameters measured are: FTS_6-2 in air+aerosol (mass_concentration_of_6_:_2_flourotelomer_sulfonic_acid_in_aerosol), FTS_8-2 in air+aerosol, PFBS in air+aerosol (mass_concentration_of_perfluorobutanesulfonic_acid_in_aerosol), PFDA in air+aerosol, PFDS in air+aerosol, PFDoDA in air+aerosol (mass_concentration_of_perfluorododecanoic_acid_in_aerosol), PFHpA in air+aerosol (mass_concentration_of_perfluoroheptanoic_acid_in_aerosol), PFHpS in air+aerosol, PFHxA in air+aerosol (mass_concentration_of_perfluorohexanoic_acid_in_aerosol), PFHxS in air+aerosol (mass_concentration_of_perfluorohexane_sulfonic_acid_in_aerosol), PFNA in air+aerosol (mass_concentration_of_perfluorononanoic_acid_in_aerosol), PFNS in air+aerosol, PFOA in air+aerosol (mass_concentration_of_perfluorooctanoic_acid_in_aerosol), PFPS in air+aerosol, PFTeDA in air+aerosol, PFTrDA in air+aerosol",
	"originatingdatacenter": "In-Situ",
	"dataversion": 1.0,
	"producttype": "mass_concentration_of_perfluorohexane_sulfonic_acid_in_aerosol",
	"program_affiliation": "EMEP, CAMP, AMAP, NILU"
}]
```

# Location

> GET /api/locations/

**Response: JSON Array of Objects:**

**location_name** (string) - name of station location

**location_id** (string) - data center unit specific identifier

**location_description** (string) - free text description of the site

**station_gaw_name** (string) - name as listed in gawsis

**station_gaw_id** (string) - gaw identifier

**station_latitude** (float) - location latitude

**station_longitude** (float) - location longitude

**Station altitude** (string) - location altitude

**Station land use** (string) - land use

**Station setting** (string) - station setting 

## Example request:

> GET /api/locations HTTPS/1.1

> Host: https://actris-rest-api.nilu.no

> Accept: application/json

## Example response:

```
[{
	"location_name": "Birkenes",
	"location_id": "NO0001R",
	"location_description": "The terrain is undulating and the site is located in a clearing with relatively free exposure to exchange of air masses by wind. The site provides data on deposition in support of effect oriented studies (surface water acidification, forest damage, material deterioration etc.). Data for the site are applied for the following monitoring programmes; EMEP, ICP Waters, ICP Forest, ICP Integrated Monitoring, ICP Materials, The Norwegian Air and Precipitation Monitoring Programme, the Norwegian Monitoring Programme on Forest Damage (OPS), and others.",
	"Station GAW-Name": "Birkenes Atmospheric Observatory",
	"Station GAW-ID": "BIR",
	"Station latitude": 58.380,
	"Station longitude": 8.250,
	"Station altitude": "220m",
	"Station land use": "Forest",
	"Station setting": "Rural"
}]
```

# Repository

> GET /api/repositories

**dc_unit_id** (int) - data center identifier

**dc_unit_acronym** (string) - acronym of data center

**dc_unit_name** (string) - data center unit full name

**dc_unit_contact** (string) - data center unit contact

**dc_unit_description** (string) - description of the data center unit

**dc_unit_url** (string) - url of data center unit
## Example request:

> GET /api/repositories HTTPS/1.1

> Host: https://actris-rest-api.nilu.no

> Accept: application/json

## Example response:

```
[{
"dc_unit_id": "2",
"dc_unit_acronym": "ARES",
"dc_unit_name": "Aerosol remote sensing data centre unit",
"dc_unit_contact": "First name, Last Name",
"dc_unit_description": "The ARES data centre unit provides a data curation and data processing service for aerosol remote sensing data coming frm lidar and photometer obsrevations.",
"dc_unit_url": "datacenter.com"
}]
```

# variable

> GET /api/variables/

**variable_id** (int) - variable identifier

**variable_name** (string) - actris variables name

**variable_description** (string) - description of variable

**wmo_code** (int) - wmo observation variable code

**cf_name** (string) - cf standard name

## Example request:

> GET /api/variables HTTPS/1.1

> Host: https://actris-rest-api.nilu.no

> Accept: application/json

## Example response:

```
[{
	"variable_id": 22,
	"variable_name": "temperature",
	"variable_description": "air temperature, kelvin",
	"wmo_code": 319,
	"cf_name": "air_temperature"

}]
```

# instrument

> GET /api/instruments/

**Instrument type** (string) - Instrument type

**Instrument manufacturer** (string) - instrument manufacturer

**Instrument model** (string) - instrument model

**Instrument name** (string) - instrument name

## Example request:

> GET /api/instruments HTTPS/1.1

> Host: https://actris-rest-api.nilu.no

> Accept: application/json

## Example response:

```
[{
	"Instrument type": "filter_absorption_photometer",
	"Instrument manufacturer": "Radiance-Research",
	"Instrument model": "PSAP-3W",
	"Instrument name": "Radiance-Research_PSAP-3W_BIR_dry"
}]
```

