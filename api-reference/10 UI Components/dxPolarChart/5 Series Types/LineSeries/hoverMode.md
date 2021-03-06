---
id: dxPolarChartSeriesTypes.linepolarseries.hoverMode
acceptValues: 'nearestPoint' | 'includePoints' | 'excludePoints' | 'none'
type: String
default: 'excludePoints'
---
---
##### shortDescription
Specifies series elements to be highlighted when a user points to the series.

---
When a user points to the series, it may react in one of the following ways depending on the value of the **hoverMode** property.

* **nearestPoint**   
The series changes its style along with the point that is nearest to the cursor.
* **includePoints**   
The series changes its style along with all the points.
* **excludePoints**   
The series changes its style, but the points do not.
* **none**   
The series does not react to pointing to it.

#####See Also#####
- [hoverStyle](/api-reference/10%20UI%20Components/dxPolarChart/5%20Series%20Types/CommonPolarChartSeries/hoverStyle '/Documentation/ApiReference/UI_Components/dxPolarChart/Series_Types/LineSeries/hoverStyle/')
- **point**.[hoverMode](/api-reference/10%20UI%20Components/dxPolarChart/5%20Series%20Types/CommonPolarChartSeries/point/hoverMode.md '/Documentation/ApiReference/UI_Components/dxPolarChart/Series_Types/LineSeries/point/#hoverMode')