# API docs

> GET /api/files

## Get a list of all files


```
> **Response: JSON Array of Objects:**

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
**originator_first** (string) - first name of data originator
**originator_last** (string) - last name of data originator
**investigator_first** (string) - first name of data investigator
**investigator_last** (string) - last name of data investigator
**submitter_first** (string) - first name of data submitter
**submitter_last** (string) - last name of data submitter
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

```

## Example request:

```

> GET /api/files **HTTPS**/1.1

> Host: https://actris-rest-api.nilu.no

> Accept: application/json

```
