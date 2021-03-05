# Calculate Value Scripts for ArcGIS ModelBuilder

*These are example scripts. Use at your own risk.*

---

## Get Spatial Reference

**Expression:**```getSR(r"%dataset%")``` 

**Code Block:**

```
def getSR(ds):
    return arcpy.Describe(ds).spatialReference.exportToText()
```

**Data type:** Spatial Reference 
 
 ---
 
 ## Get Extent
 
 **Expression:**```getExtent(r"%dataset%")``` 

**Code Block:**

```
def getExtent(ds):
    ex = arcpy.Describe(ds).extent
    return "{} {} {} {}".format(ex.XMin, ex.YMin, ex.XMax, ex.YMax)
```

**Data type:** Extent
 
 ---
  
 ## Get Environment
 
 **Expression:**```arcpy.GetSystemEnvironment("ENV_VARIABLE")```

**Code Block:** (none)

**Data type:** Variant (or whatever you need it to be)
 
 ---
