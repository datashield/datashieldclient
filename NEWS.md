# datashieldclient 3.0.0

## Main changes

* The syntax of the commands has now been drastically simplified for all the client functions e.g. previously to generate a 1-dimensional table of for example the variabl `DIS_CVA` held in data frame `D` we would   have written:  
  _`ds.table1d(datasources=opals, xvect=quote(D$DIS_CVA))`_  
  Now we write:  
  _`ds.table1D(x='D$DIS_CVA')`_  
  This was possible because in this latest version after the user logs in the opal login object is retrieved internally 
  and the variable name provided a string characted is also `quoted` internally before it is passed on to the server side
  function.

* Some functions have been removed either because they were not safe according to DataSHIELD privacy and confidentiality   preserving principles or because their functionality is now available within other functions.

* __As a consequence of the above changes old scripts would need to be updated to adopt the new
 naming and syntax. The table under the section 'summary of the changes' will tell what functions are new or got their
 name changed. So all users should update their old script to avoid errors resulting from using obsolete functions,
 funtion names or syntax.__ 

## List of packages and functions in the version 3.0.0
There are now four packages. The name of the packages and their functions can be viewed [here](https://wikis.bris.ac.uk/display/DSDEV/List+of+Packages+and+functions+currently+available "Title").

## Summary of the changes
|Previous name of the function|Name in datashieldclient 3.0.0|Status|
|-----------------------------|------------------------|------|
ds.append2df|-|removed|
-|ds.asFactor|new|
ds.asCharacter|ds.asCharacter|-|
ds.asList|ds.asList|-|
ds.asMatrix|ds.asMatrix|-|
ds.asNull|-|removed|
ds.asNumeric|ds.asNumeric|-|
ds.assign|ds.assign|-|
ds.c|ds.c|-|
ds.cbind|ds.cbind|-|
ds.changerefgroup|ds.changeRefGroup|-|
ds.checkvar|-|removed|
ds.class|ds.class|-|
ds.colnames|ds.colnames|
ds.complete.cases|-|removed|
ds.contourplot|ds.contourPlot|-|
-|ds.cor|new|
-|ds.corTest|new|
-|ds.cov|new|
ds.createfactor|-|removed|
ds.data.frame|ds.dataframe|-|
ds.densitygrid|ds.densityGrid|-|
ds.dim|ds.dim|-|
ds.exists|ds.exists|-|
ds.exp|ds.exp|-|
ds.fac2num|-|removed|
-|ds.gee|new|
ds.glm|ds.glm|-|
ds.heatmapplot|ds.heatmapPlot|-|
ds.histogram|ds.histogram|-|
ds.inform|-|removed|
ds.is.character|-|removed|
ds.is.factor|-|removed|
ds.is.null|-|removed|
ds.is.numeric|-|removed|
ds.isNA|ds.isNA|-|
ds.isPresent|-|removed|
ds.isValid|ds.isValid|-|
ds.length|ds.length|-|
ds.levels|ds.levels|-|
ds.list|ds.list|-|
ds.log|ds.log|-|
ds.makeBinary|-|removed|
ds.mean|ds.mean|-|
ds.meanByClass|ds.meanByClass|-|
ds.names|ds.names|-|
ds.NROW|-|removed|
ds.product|-|removed|
ds.quantilemean|ds.quantileMean|-|
ds.range|-|removed|
ds.recodelevels|ds.recodeLevels|-|
ds.rowcolCalc|ds.rowColCalc|-|
ds.subclass|ds.subclass|-|
ds.subset|ds.subset|-|
ds.sum|-|removed|
ds.summary|ds.summary|-|
ds.t.test|ds.tTest|-
ds.table1d|ds.table1D|-
ds.table2d|ds.table2D|-
ds.var|ds.var|-|
-|ds.vectorCalc|new|
