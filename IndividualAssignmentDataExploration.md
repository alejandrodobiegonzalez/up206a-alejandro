```python
import geopandas as gpd
```


```python
council = gpd.read_file('../../data/MetroStations/lacitycouncildistrict(2012).shp')
```


    ---------------------------------------------------------------------------

    CPLE_OpenFailedError                      Traceback (most recent call last)

    fiona/_shim.pyx in fiona._shim.gdal_open_vector()


    fiona/_err.pyx in fiona._err.exc_wrap_pointer()


    CPLE_OpenFailedError: Unable to open ../../data/MetroStations/lacitycouncildistrict(2012).shx or ../../data/MetroStations/lacitycouncildistrict(2012).SHX. Set SHAPE_RESTORE_SHX config option to YES to restore or create it.

    
    During handling of the above exception, another exception occurred:


    DriverError                               Traceback (most recent call last)

    <ipython-input-2-e2859c6a73b2> in <module>
    ----> 1 council = gpd.read_file('../../data/MetroStations/lacitycouncildistrict(2012).shp')
    

    /opt/conda/lib/python3.8/site-packages/geopandas/io/file.py in _read_file(filename, bbox, mask, rows, **kwargs)
         94 
         95     with fiona_env():
    ---> 96         with reader(path_or_bytes, **kwargs) as features:
         97 
         98             # In a future Fiona release the crs attribute of features will


    /opt/conda/lib/python3.8/site-packages/fiona/env.py in wrapper(*args, **kwargs)
        398     def wrapper(*args, **kwargs):
        399         if local._env:
    --> 400             return f(*args, **kwargs)
        401         else:
        402             if isinstance(args[0], str):


    /opt/conda/lib/python3.8/site-packages/fiona/__init__.py in open(fp, mode, driver, schema, crs, encoding, layer, vfs, enabled_drivers, crs_wkt, **kwargs)
        254 
        255         if mode in ('a', 'r'):
    --> 256             c = Collection(path, mode, driver=driver, encoding=encoding,
        257                            layer=layer, enabled_drivers=enabled_drivers, **kwargs)
        258         elif mode == 'w':


    /opt/conda/lib/python3.8/site-packages/fiona/collection.py in __init__(self, path, mode, driver, schema, crs, encoding, layer, vsi, archive, enabled_drivers, crs_wkt, ignore_fields, ignore_geometry, **kwargs)
        162             if self.mode == 'r':
        163                 self.session = Session()
    --> 164                 self.session.start(self, **kwargs)
        165             elif self.mode in ('a', 'w'):
        166                 self.session = WritingSession()


    fiona/ogrext.pyx in fiona.ogrext.Session.start()


    fiona/_shim.pyx in fiona._shim.gdal_open_vector()


    DriverError: Unable to open ../../data/MetroStations/lacitycouncildistrict(2012).shx or ../../data/MetroStations/lacitycouncildistrict(2012).SHX. Set SHAPE_RESTORE_SHX config option to YES to restore or create it.



```python
yes
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-3-084d24bbed96> in <module>
    ----> 1 yes
    

    NameError: name 'yes' is not defined



```python
council = gpd.read_file('../../data/MetroStations/lacitycouncildistrict_2012.shp')
```


    ---------------------------------------------------------------------------

    CPLE_OpenFailedError                      Traceback (most recent call last)

    fiona/_shim.pyx in fiona._shim.gdal_open_vector()


    fiona/_err.pyx in fiona._err.exc_wrap_pointer()


    CPLE_OpenFailedError: Unable to open ../../data/MetroStations/lacitycouncildistrict_2012.shx or ../../data/MetroStations/lacitycouncildistrict_2012.SHX. Set SHAPE_RESTORE_SHX config option to YES to restore or create it.

    
    During handling of the above exception, another exception occurred:


    DriverError                               Traceback (most recent call last)

    <ipython-input-4-5d7477ad3333> in <module>
    ----> 1 council = gpd.read_file('../../data/MetroStations/lacitycouncildistrict_2012.shp')
    

    /opt/conda/lib/python3.8/site-packages/geopandas/io/file.py in _read_file(filename, bbox, mask, rows, **kwargs)
         94 
         95     with fiona_env():
    ---> 96         with reader(path_or_bytes, **kwargs) as features:
         97 
         98             # In a future Fiona release the crs attribute of features will


    /opt/conda/lib/python3.8/site-packages/fiona/env.py in wrapper(*args, **kwargs)
        398     def wrapper(*args, **kwargs):
        399         if local._env:
    --> 400             return f(*args, **kwargs)
        401         else:
        402             if isinstance(args[0], str):


    /opt/conda/lib/python3.8/site-packages/fiona/__init__.py in open(fp, mode, driver, schema, crs, encoding, layer, vfs, enabled_drivers, crs_wkt, **kwargs)
        254 
        255         if mode in ('a', 'r'):
    --> 256             c = Collection(path, mode, driver=driver, encoding=encoding,
        257                            layer=layer, enabled_drivers=enabled_drivers, **kwargs)
        258         elif mode == 'w':


    /opt/conda/lib/python3.8/site-packages/fiona/collection.py in __init__(self, path, mode, driver, schema, crs, encoding, layer, vsi, archive, enabled_drivers, crs_wkt, ignore_fields, ignore_geometry, **kwargs)
        162             if self.mode == 'r':
        163                 self.session = Session()
    --> 164                 self.session.start(self, **kwargs)
        165             elif self.mode in ('a', 'w'):
        166                 self.session = WritingSession()


    fiona/ogrext.pyx in fiona.ogrext.Session.start()


    fiona/_shim.pyx in fiona._shim.gdal_open_vector()


    DriverError: Unable to open ../../data/MetroStations/lacitycouncildistrict_2012.shx or ../../data/MetroStations/lacitycouncildistrict_2012.SHX. Set SHAPE_RESTORE_SHX config option to YES to restore or create it.



```python
import geopandas as gpd
```


```python
council = gpd.read_file('../../data/MetroStations/lacitycouncildistrict_2012.shp')
```


```python
type(council)
```




    geopandas.geodataframe.GeoDataFrame




```python
council.head
```




    <bound method NDFrame.head of                                 slug                                 set  \
    0   10-la-city-council-district-2012  L.A. City Council Districts (2012)   
    1   11-la-city-council-district-2012  L.A. City Council Districts (2012)   
    2   12-la-city-council-district-2012  L.A. City Council Districts (2012)   
    3   13-la-city-council-district-2012  L.A. City Council Districts (2012)   
    4   14-la-city-council-district-2012  L.A. City Council Districts (2012)   
    5   15-la-city-council-district-2012  L.A. City Council Districts (2012)   
    6    1-la-city-council-district-2012  L.A. City Council Districts (2012)   
    7    2-la-city-council-district-2012  L.A. City Council Districts (2012)   
    8    3-la-city-council-district-2012  L.A. City Council Districts (2012)   
    9    4-la-city-council-district-2012  L.A. City Council Districts (2012)   
    10   5-la-city-council-district-2012  L.A. City Council Districts (2012)   
    11   6-la-city-council-district-2012  L.A. City Council Districts (2012)   
    12   7-la-city-council-district-2012  L.A. City Council Districts (2012)   
    13   8-la-city-council-district-2012  L.A. City Council Districts (2012)   
    14   9-la-city-council-district-2012  L.A. City Council Districts (2012)   
    
                                     kind external_i name  \
    0   L.A. City Council District (2012)         10   10   
    1   L.A. City Council District (2012)         11   11   
    2   L.A. City Council District (2012)         12   12   
    3   L.A. City Council District (2012)         13   13   
    4   L.A. City Council District (2012)         14   14   
    5   L.A. City Council District (2012)         15   15   
    6   L.A. City Council District (2012)          1    1   
    7   L.A. City Council District (2012)          2    2   
    8   L.A. City Council District (2012)          3    3   
    9   L.A. City Council District (2012)          4    4   
    10  L.A. City Council District (2012)          5    5   
    11  L.A. City Council District (2012)          6    6   
    12  L.A. City Council District (2012)          7    7   
    13  L.A. City Council District (2012)          8    8   
    14  L.A. City Council District (2012)          9    9   
    
                                  display_na DISTRICT  \
    0   10 L.A. City Council District (2012)       10   
    1   11 L.A. City Council District (2012)       11   
    2   12 L.A. City Council District (2012)       12   
    3   13 L.A. City Council District (2012)       13   
    4   14 L.A. City Council District (2012)       14   
    5   15 L.A. City Council District (2012)       15   
    6    1 L.A. City Council District (2012)       01   
    7    2 L.A. City Council District (2012)       02   
    8    3 L.A. City Council District (2012)       03   
    9    4 L.A. City Council District (2012)       04   
    10   5 L.A. City Council District (2012)       05   
    11   6 L.A. City Council District (2012)       06   
    12   7 L.A. City Council District (2012)       07   
    13   8 L.A. City Council District (2012)       08   
    14   9 L.A. City Council District (2012)       09   
    
                                                 geometry  
    0   POLYGON ((-118.29166 34.06905, -118.29164 34.0...  
    1   POLYGON ((-118.35846 33.98304, -118.35861 33.9...  
    2   POLYGON ((-118.46805 34.28553, -118.46924 34.2...  
    3   POLYGON ((-118.27834 34.15320, -118.27561 34.1...  
    4   POLYGON ((-118.22993 34.12134, -118.22985 34.1...  
    5   POLYGON ((-118.25413 33.94187, -118.25411 33.9...  
    6   POLYGON ((-118.29998 34.05222, -118.29100 34.0...  
    7   POLYGON ((-118.43998 34.17575, -118.43998 34.1...  
    8   POLYGON ((-118.54609 34.22058, -118.54603 34.2...  
    9   POLYGON ((-118.35631 34.16877, -118.35625 34.1...  
    10  POLYGON ((-118.39091 34.03121, -118.38776 34.0...  
    11  POLYGON ((-118.36647 34.22992, -118.35921 34.2...  
    12  POLYGON ((-118.50664 34.33517, -118.50381 34.3...  
    13  POLYGON ((-118.28401 34.03703, -118.28396 34.0...  
    14  POLYGON ((-118.26947 34.03594, -118.27082 34.0...  >




```python
council.shape
```




    (15, 8)




```python
council.info()
```

    <class 'geopandas.geodataframe.GeoDataFrame'>
    RangeIndex: 15 entries, 0 to 14
    Data columns (total 8 columns):
     #   Column      Non-Null Count  Dtype   
    ---  ------      --------------  -----   
     0   slug        15 non-null     object  
     1   set         15 non-null     object  
     2   kind        15 non-null     object  
     3   external_i  15 non-null     object  
     4   name        15 non-null     object  
     5   display_na  15 non-null     object  
     6   DISTRICT    15 non-null     object  
     7   geometry    15 non-null     geometry
    dtypes: geometry(1), object(7)
    memory usage: 1.1+ KB



```python
council.columns.to_list()
```




    ['slug',
     'set',
     'kind',
     'external_i',
     'name',
     'display_na',
     'DISTRICT',
     'geometry']




```python
council.plot()
```




    <matplotlib.axes._subplots.AxesSubplot at 0x7f2f542d56d0>




    
![png](output_11_1.png)
    



```python

```
