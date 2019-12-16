# Migration guide

## JFreeChart migration guide from 1.0.x to 1.5.x

### RENAMING

1. ```ChartUtilities``` becomes ```ChartUtils```
2. ```DatasetUtilities``` becomes ```DatasetUtils```
3. ```ShapeUtilities``` becomes ```ShapeUtils```
4. ```TextUtilities``` becomes ```TextUtils```

### PATH RENAMING

(```org.jfree.ui``` became ```org.jfree.chart.ui```)
1. ```org.jfree.ui.RectangleInsets``` becomes ```org.jfree.chart.ui.RectangleInsets```
2. ```org.jfree.ui.RectangleEdge``` becomes ```org.jfree.chart.ui.RectangleEdge```
3. ```org.jfree.chart.util.ParamChecks``` becomes ```org.jfree.chart.util.Args```
4. ```org.jfree.ui.RefineryUtilities``` becomes ``` org.jfree.chart.ui.UIUtils```


### METHOD RENAMING

(```getBase/setBase``` methods renamed to ```getDefault/setDefault```)
1. ```renderer.setShapesVisible()``` becomes ```renderer.setDefaultShapesVisible()```
2. ```renderer.setBaseItemLabelGenerator``` becomes ```renderer.setDefaultItemLabelGenerator()```



### BEHAVIORAL CHANGE

1. Using both a ```MouseHandlerFX``` and a ```ChartMouseListenerFX``` on the same chart, the ```ChartMouseListenerFX``` now gets fired last



### DISAPPEARED 

1. (Stacked)BarRenderer3D                            ;; Get from OrsonCharts
2. Axis3D                                            ;; Get from OrsonCharts                     
3. org.jfree.ui.about                                ;; Get from JCommon


### MIGRATIONS

1. ``` isPointInReact``` moved from ```AbstractXYItemRenderer``` to ```ShapeUtils```
2. All classes from ```JCommon``` that are used by ```JFreeChart``` have integrated within the ```JFreeChart``` jar file within a different package
3. All the classes relating to pseudo-3D charts have been removed, the 3D charts are maintained by ```Orson Charts```
4. The ```SegmentedTimeline``` class has been removed.
