# Install Package
```python
pip install quickplot
```

# Package
### quickplot.bar

**quickplot.****bar**** ****(**_**table, key_column, value_column, title= None, x_label= None, y_label= None, frame_dimensions= (12, 9), e****rror_column= None, show_mean= True, annotate= True, process_data_type= True,  **kwargs)**_
**
Draws a bar chart. Used to present a digestible comparison of values varying either by category or by a short range of periodic intervals.


**Parameters:   **
**table **: _Pandas DataFrame Object_
Input dataset.
**key_column **: _string_
Column name attributing to chart keys placed on the x-axis.
**value_column **: _string_
Column name attributing to chart values placed on the y-axis.
**title** : _string__, optional_
Chart title.
**x_label** : _string__, optional_
X-axis label.
**y_label **: _string__, optional_
Y-axis label.
**frame_dimensions **: _tuple of integers or floats, optional_
Length and width of the chart.
**error_column **: _string, optional_
Column name attributing to the confidence interval plotted as capped error bar lines.
**show_mean **: _bool, optional_
When show_mean is used, a dashed line is plotted onto the chart corresponding to the mean value across keys.
**annotate **: _bool, optional_
When annotate is used, text annotation is plotted onto the chart corresponsind to the value of each key as well as the mean value when applicable.
**process_data_type** : _bool, optional_
When process_data_type is used, the value  and error columns passed are converted to the float data type.
**kwargs **: _key, value mappings_
Other keyword arguments are passed through to [matplotlib.pyplot.bar()](https://matplotlib.org/3.2.1/api/_as_gen/matplotlib.pyplot.bar.html).

Returns:    
**fig, ax **: _Matplotlib figure and axes._
Matplotlib figure and axis objects with chart drawn onto them.

### quickplot.segmented_bar**

**quickplot.****segmented_bar**** ****(**_**table, key_column, value_column, title= None, x_label= None, y_label= None, frame_dimensions= (12****, 9), error_column= None, show_mean= True, annotate= True, process_data_type= True, **kwargs)**_
**
Draws a segmented bar chart. Used to display values collected over two levels of aggregation.


**Parameters:   **
**table **: _Pandas DataFrame Object_
Input dataset.**
**key_column **: _string_
Column name attributing to chart keys placed on the x-axis.
**value_column **: _string_
Column name attributing to chart values placed on the y-axis.
**segment_column** : _string_
Column name attributing to key groups.
**title** : _string__, optional_
Chart title.
**x_label** : _string__, optional_
X-axis label.
**y_label **: _string__, optional_
Y-axis label.
**frame_dimensions **: _tuple of integers or floats, optional_
Length and width of the chart.
**error_column **: _string, optional_
Column name attributing to the confidence interval plotted as capped error bar lines.
**show_mean **: _bool, optional_
When show_mean is used, a dashed line is plotted onto the chart corresponding to the mean value across keys.
**annotate **: _bool, optional_
When annotate is used, text annotation is plotted onto the chart corresponsind to the value of each key as well as the mean value when applicable.
**process_data_type** : _bool, optional_
When process_data_type is used, the value  and error columns passed are converted to the float data type.
**kwargs **: _key, value mappings_
Other keyword arguments are passed through to [matplotlib.pyplot.bar()](https://matplotlib.org/3.2.1/api/_as_gen/matplotlib.pyplot.bar.html).

Returns:    
**fig, ax **: _Matplotlib figure and axes._
Matplotlib figure and axis objects with the chart drawn onto them.

### quickplot.plot_distribution

**quickplot.****plot_distribution**** ****(**_**table, value_column, segment_column= None, title= None, x_label= None, y_label= None, frame_dim****ensions= (12, 9), kde= False, bins= None, process_data_type= True, log10_transform= False,  **kwargs)**_
**
Draws either the kernel density estimate of a distribution with an accompanying frequency histogram for a single feaure across each listed segment or the frequency histogram alone. Used to visualize the shape and characteristics of one or several value distributions.


**Parameters:   **
**table **: _Pandas DataFrame Object_
Input dataset.**
**value_column **: _string_
Column name attributing to chart values placed on the y-axis.
**segment_column** : _string__, optional_
Column name attributing to key groups.
**title** : _string__, optional_
Chart title.
**x_label** : _string__, optional_
X-axis label.
**y_label **: _string__, optional_
Y-axis label.
**frame_dimensions **: _tuple of integers or floats, optional_
Length and width of the chart.
**kde **: _bool, optional_
When kde is used, a kernel density estimate is plotted with an accompanying frequency histogram. Alternatively, the frequency histogram alone is plotted.
**bins **: _int, optional_
Manually sets the amount of bins placed on each histogram. When None, Seaborn finds a suitable default using a reference rule.
**process_data_type** : _bool, optional_
When process_data_type is used, all  columns except for a passed segment column are converted to the float data type.
**log10_transform** : _bool, optional_
When log10_transform is used, all columns except for a passed segment column are transformed onto the log10 scale. When 0 values are present in any column, the column values are increased by 1 prior to transformation. 
**kwargs **: _key, value mappings_
Other keyword arguments are passed through to [seaborn.distplot()](https://seaborn.pydata.org/generated/seaborn.distplot.html).

Returns:    
**fig, ax **: _Matplotlib figure and axes._
Matplotlib figure and axis objects with the chart drawn onto them.

### quickplot.plot_distribution_summary

**quickplot.****plot_distribution**** ****(**_**table, value_column, segment_column= None, title= None, x_label= None, y_label= None****, frame_dimensions= ****'auto', horizontal= True, violin= False, process_data_type= True, log10_transform= False,  **kwargs)**_
**
Draws either a violin plot or a box plot for a single feature across each listed segment. Used to visualize the shape and characteristics of one or several value distributions.

**Parameters:   **
**table **: _Pandas DataFrame Object_
Input dataset.**
**value_column **: _string_
Column name attributing to chart values placed on the y-axis.
**segment_column** : _string__, optional_
Column name attributing to key groups.
**title** : _string__, optional_
Chart title.
**x_label** : _string__, optional_
X-axis label.
**y_label **: _string__, optional_
Y-axis label.
**frame_dimensions **: _'auto' or a tuple of integers or floats, optional_
Length and width of the chart. When 'auto', a default setting is placed depending on the orientation and type of chart used.
**horizontal **: _bool, optional_
When horizontal is used, the plotted chart will be oriented horizontally. Otherwise, the chart will be oriented vertically. 
**violin **: _bool, optional_
When violin is used, a violin chart is plotted. Alternatively, a box chart is plotted.
**process_data_type** : _bool, optional_
When process_data_type is used, all  columns except for a passed segment column are converted to the float data type.
**log10_transform** : _bool, optional_
When log10_transform is used, all  columns except for a passed segment column are transformed onto the log10 scale. When 0 values are present in any column, the column values are increased by 1 prior to transformation. 
**kwargs **: _key, value mappings_
Other keyword arguments are passed through to [seaborn.distplot()](https://seaborn.pydata.org/generated/seaborn.distplot.html).

Returns:    
**fig, ax **: _Matplotlib figure and axes._
Matplotlib figure and axis objects with the chart drawn onto them.

### quickplot.scatter**

**quickplot.****scatter**** ****(**_**table, x_column, y_column,**** segment_column= None,**** title= None, x_label= None, y_label= None, fr****ame_dimensions= (12, 9), process_data_type= True, log10_transform= False,  **kwargs)**_
**
Draws a scatter plot for two features across all listed segments. Used to visualize the relational characteristics present in any two features.

**Parameters:   **
**table **: _Pandas DataFrame Object_
Input dataset.**
**x_column **: _string_
Column name attributing to chart keys placed on the x-axis.
**y_column **: _string_
Column name attributing to chart values placed on the y-axis.
**segment_column** : _string, optional_
Column name attributing to key groups.
**title** : _string__, optional_
Chart title.
**x_label** : _string__, optional_
X-axis label.
**y_label **: _string__, optional_
Y-axis label.
**frame_dimensions **: _tuple of integers or floats, optional_
Length and width of the chart.
**process_data_type** : _bool, optional_
When process_data_type is used, all  columns except for a passed segment column are converted to the float data type.
**log10_transform** : _bool, optional_
When log10_transform is used, all columns except for a passed segment column are transformed onto the log10 scale. When 0 values are present in any column, the column values are increased by 1 prior to transformation. 
**kwargs **: _key, value mappings_
Other keyword arguments are passed through to [seaborn.scatterplot()](https://seaborn.pydata.org/generated/seaborn.scatterplot.html).


Returns:    
**fig, ax **: _Matplotlib figure and axes._
Matplotlib figure and axis objects with the chart drawn onto them.

### quickplot.correlation_heatmap

**quickplot.****heatmap**** ****(**_**table, title= None, ****frame_dimensions= (12, 9), ****annotate= True, color_map= 'Diverging', color_blind= Fals****e, segment_column= None, segment= None, process_data_type= True, log10_transform= False****,**** **kwargs**_**)**
**
Draws a heatmap detailing correlation values across all numerical features in the presented dataset. Used to summarize feature interactions and the direction of feature relationships. 

**Parameters:   **
**table **: _Pandas DataFrame Object_
Input dataset.**
**title** : _string__, optional_
Chart title.**
**frame_dimensions **: _tuple of integers or floats, optional_
Length and width of the chart.
**annotate **: _bool, optional_
When annotate is used, text annotation is plotted onto the chart corresponsing to the value of cell in the correlation matrix.
**color_map **: _'Diverging' or strin__g, optional_
When set to_ 'Diverging',_ a default diverging color map is applied. Alternatively, this parameter could be set to an [existing Matplotlib color map](https://matplotlib.org/tutorials/colors/colormaps.html).
**color_blind **:** **_bool, optional_
When color_blind is used and color_map is set to _'Diverging'_, the [viridis](https://gotellilab.github.io/GotelliLabMeetingHacks/NickGotelli/ViridisColorPalette.html) color palette is applied as the it translates well to grayscale. 
**segment_column** : _string, optional_
Column name attributing to key groups. Same output as _None_ when the segment argument is also _None_.
**segment **: _string_ _(category present in segment column), optional_
When an applicable segment column is passed and an applicable segment is passed, a correlation heatmap for the given segment alone is generated.
**process_data_type** : _bool, optional_
When process_data_type is used, all  columns except for a passed segment column are converted to the float data type.
**log10_transform** : _bool, optional_
When log10_transform is used, all  columns except for a passed segment column are transformed onto the log10 scale. When 0 values are present in any column, the column values are increased by 1 prior to transformation. 
**kwargs **: _key, value mappings_
Other keyword arguments are passed through to [seaborn.heatmap()](https://seaborn.pydata.org/generated/seaborn.heatmap.html).


Returns:    
**fig, ax **: _Matplotlib figure and axes._
Matplotlib figure and axis objects with the chart drawn onto them.

### quickplot.pairplot

**quickplot.****pairplot**** ****(**_**table, segment_column= None, title= None, frame_dimensions= (12, 10), kde= 'auto',**_** process_data_type= True, log10_transform= False, **_** **kwargs**_**)**
**
Draws scatter plots for every pair of features present in a data set and either a kernel density estimate or histogram for every individual feature present across all listed segments. Used to present distribution and relational characteristics across a feature set.

**Parameters:   **
**table **: _Pandas DataFrame Object_
Input dataset.**
**segment_column** : _string_
Column name attributing to key groups.
**title** : _string__, optional_
Chart title.**
**frame_dimensions **: _tuple of integers or floats, optional_
Length and width of the chart.
**hist : **_bool, optional_
When hist is used, the histograms are plotted across the diagonal.
**process_data_type** : _bool, optional_
When process_data_type is used, all  columns except for a passed segment column are converted to the float data type.
**log10_transform** : _bool, optional_
When log10_transform is used, all  columns except for a passed segment column are transformed onto the log10 scale. When 0 values are present in any column, the column values are increased by 1 prior to transformation. 
**kwargs **: _key, value mappings_
Other keyword arguments are passed through to [seaborn.pairplot()](https://seaborn.pydata.org/generated/seaborn.pairplot.html).


Returns:    
**fig, ax **: _Matplotlib figure and axes._
Matplotlib figure and axis objects with the chart drawn onto them.


# Change Log
0.2.4 2021/04/11

- Added package to PyPI. Use pip instlall quickplot to run.
- Initial public commit.





