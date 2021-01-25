# NSG 4G celldb
NSG 4G celldb is a crowdsourced 4G cell database for Network Signal Guru Android app.
## Explanation:
Cell database is a CSV file containing information of 4G eNbs (Towers) only from operators in Germany (262-01, -02 & -03). All values are comma-separated.
### Table structure:
* __Cellname__ -> Name for the Cell ([Operator]-[eNb-ID], e.g. VF-44855)
* __Longitude__ -> Longitude coordinate of cell location (must be exactly 7 digits after '.', e.g. 50.1234567)
* __Latitude__ -> Latitude coordinate of cell location (must be exactly 7 digits after '.', e.g. 60.1234567)
* __PCI__ -> Physical Cell Identifier (__always__ 3 digits long, if less -> add leading '0', e.g. 008)
* __EARFCN__ -> Frequency ID (e.g. 101, 6300, etc.)
* __ECellID__ -> Unique Cell ID (e.g. 10566783)
* __Azimuth__ -> Direction of transmission via angle indication (e.g. 3 sector tower looking at 0°, 120° & 240°, put in the angles without the '°')
In general, data from official STOBs (BNetzA), Cellmapper and NSG can be combined to fill the required fields in the db cellfile.
