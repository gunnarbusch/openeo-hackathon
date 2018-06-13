# Solution for Task 5

Process graph for the openEO Google Earth Engine back-end:
```
{
  "process_id":"zonal_statistics",
  "args":{
    "imagery":{
      "process_id":"filter_bands",
      "args":{
        "imagery":{
          "process_id":"filter_daterange",
          "args":{
            "imagery":{
              "process_id":"filter_bbox",
              "args":{
                "imagery":{
                  "product_id":"COPERNICUS/S2"
                },
                "srs":"EPSG:4326",
                "left":16.138916,
                "right":16.524124,
                "top":48.320647,
                "bottom":48.1386
              }
            },
            "from":"2018-01-01",
            "to":"2018-01-15"
          }
        },
        "bands":"B8"
      }
    },
    "regions":"polygon.json",
    "func":"mean"
  }
}
```