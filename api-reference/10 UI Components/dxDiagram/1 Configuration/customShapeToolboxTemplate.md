---
id: dxDiagram.Options.customShapeToolboxTemplate
type: template
---
---
##### shortDescription
Specifies a custom template for shapes in the toolbox.

##### param(container): dxSVGElement
#include common-ref-elementparam with { element: "shape" }

##### param(data): Object
Information about the currently processed shape.

##### field(data.item): dxDiagramShape
Information about the currently processed shape.

##### return: void
<!-- Description goes here -->

---
The template content must be presented as SVG elements.

Use the [toolboxTemplate](/api-reference/10%20UI%20Components/dxDiagram/1%20Configuration/customShapes/toolboxTemplate.md '/Documentation/ApiReference/UI_Components/dxDiagram/Configuration/customShapes/#toolboxTemplate') property to define a template for each shape in the toolbox.

#include common-demobutton with {
    url: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/Diagram/CustomShapesWithTemplatesWithEditing/"
}

#####See Also#####
- [Custom Templates](/concepts/05%20UI%20Components/zz%20Common/30%20Templates/10%20Custom%20Templates.md '/Documentation/Guide/UI_Components/Common/Templates/#Custom_Templates')
