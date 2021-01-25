# NSG 4G celldb

NSG 4G celldb is a crowdsourced 4G cell database for Network Signal Guru Android app. Contribute by adding tower data from towers in your area. Create a pull request with your added towers. Please check, if the file is valid and working in NSG before opening any request. 

## Why does this exist?

Cell database is a CSV file containing information of 4G eNbs (4G Towers). All values are comma-separated. This file can be imported into NSG to display tower location, cell sectors and their respective azimuth (quite like cellmapper does).

[](https://raw.githubusercontent.com/Henrocker/NSG-4G-celldb/main/example.PNG)

### Table structure:

* __Cellname__ -> Name for the Cell ([Operator]-[eNb-ID], e.g. VF-44855)
* __Longitude__ -> Longitude coordinate of cell location (must be exactly seven digits after '.', e.g. 50.1234567)
* __Latitude__ -> Latitude coordinate of cell location (must be exactly seven digits after '.', e.g. 60.1234567)
* __PCI__ -> Physical Cell Identifier (__always__ three digits long, if less -> add leading '0', e.g. 008)
* __EARFCN__ -> Frequency ID (e.g. 101, 6300, etc.)
* __ECellID__ -> Unique Cell ID (e.g. 10566783)
* __Azimuth__ -> Direction of transmission via angle indication (e.g. for a three sector tower looking at 0°, 120° & 240°, put in the angles without the '°')

In general, data from official STOBs (BNetzA), Cellmapper and NSG can be combined to fill the required fields in the db cellfile. See the existing celldb for some orientation on formatting and data requirements.

## Links

Visit the [official documentation](https://m.qtrun.com/help/111CellFileBasics.html) to learn more.
