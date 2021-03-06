---
id: dxDataGrid.Options.remoteOperations.groupPaging
type: Boolean
default: false
---
---
##### shortDescription
Specifies whether paging by groups should be performed on the server side.

---
Remote group paging allows you to load groups from a remote source in portions. This feature speeds up grouping because the DataGrid transmits less data. However, requests are more frequent because the DataGrid sends several requests each time a user expands a group or sorts/filters data.

Remote group paging has the following specificities:

- All other operations (filtering, paging, grouping, sorting, and summaries calculation) should also be remote.

- Remote group paging does not apply if you set the **grouping**.[autoExpandAll](/api-reference/10%20UI%20Components/dxDataGrid/1%20Configuration/grouping/autoExpandAll.md '/Documentation/ApiReference/UI_Components/dxDataGrid/Configuration/grouping/#autoExpandAll') property to **true** or call the [expandAll(groupIndex)](/api-reference/10%20UI%20Components/dxDataGrid/3%20Methods/expandAll(groupIndex).md '/Documentation/ApiReference/UI_Components/dxDataGrid/Methods/#expandAllgroupIndex') method.

#include common-demobutton with {
    url: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/DataGrid/RemoteGrouping/"
}