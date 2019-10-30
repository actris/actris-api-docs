# Files

## Get list of all files

```
GET /api/files
```

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

**Status Codes:	** 500 Internal Server Error
              error-code (int) – application error

## Example request:

```
GET /api/files **HTTPS**/1.1

Host: https://actris-rest-api.nilu.no

Accept: application/json
```

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
	"platform": "station",
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
	"producttype": "mass_concentration_of_perfluorohexane_sulfonic_acid_in_aerosol"
}]
```



