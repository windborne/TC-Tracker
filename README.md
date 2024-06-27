# TC Tracker for WeatherMesh

Code was taken from CyTrack (https://github.com/apalarcon/CyTRACK) and modifications were made to work with WeatherMesh datasets. 

CyTrack code has a GPLv3 license. See License on README page => https://github.com/apalarcon/CyTRACK?tab=readme-ov-file

This paper describes the tracker methods and verification to other TC trackers => https://www.sciencedirect.com/science/article/pii/S1364815224000884

Settings for tracker can be found in test_CyTRACK.cfg. Currently setup to track TCs over the Northern Hemisphere. 

## Only modifications that need to be made in the test_CyTRACK.cfg are:
```
-path_data_terr_source
-path_data_source
-path_data_source_upper
-search_region
-search_limits
-begin_year, begin_month, begin_day, begin_hour
-end_year, end_month, end_day, end_hour
```

* Details on the tracker
```
python run_CyTRACK.py -cth t
```
* Command to run the tracker
```
python run_CyTRACK.py -pf test_CyTRACK.cfg
```
* Command to run the tracker with multiple CPUs
```
mpirun -np #cpus python run_CyTRACK.py -pf test_CyTRACK.cfg
```
