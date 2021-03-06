A label is an element that accompanies a [node](/concepts/05%20UI%20Components/Sankey/05%20Nodes%20and%20Links/00%20Overview.md '/Documentation/Guide/UI_Components/Sankey/Nodes_and_Links/Overview/') and displays the node's title or custom data.

![Sankey - Node Labels](/images/Sankey/visual_elements/node_labels.png)

Properties that configure node labels are collected in the [label](/api-reference/10%20UI%20Components/dxSankey/1%20Configuration/label '/Documentation/ApiReference/UI_Components/dxSankey/Configuration/label/') object. Refer to its description in the API reference and to other articles in this section for information on node label settings.

---
##### jQuery

    <!--JavaScript-->$(function() {
        $("#sankeyContainer").dxSankey({
            // ...
            label: {
                // Settings for all node labels
            }
        });
    });

##### Angular

    <!--HTML--><dx-sankey ... >
        <dxo-label ... >
            <!-- Settings for all node labels -->
        </dxo-label>
    </dx-sankey>

    <!--TypeScript-->
    import { DxSankeyModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxSankeyModule
        ],
        // ...
    })

##### Vue

    <!-- tab: App.vue -->
    <template> 
        <DxSankey ... >
            <DxLabel <!-- Settings for all node labels --> />
        </DxSankey>
    </template>

    <script>
    import DxSankey, { DxLabel } from 'devextreme-vue/sankey';

    export default {
        components: {
            DxSankey,
            DxLabel
        }
    }
    </script>

##### React

    <!-- tab: App.js -->
    import React from 'react';
    import Sankey, { Label } from 'devextreme-react/sankey';

    class App extends React.Component {
        render() {
            return (
                <Sankey ... >
                    <Label {/* Settings for all node labels */} />
                </Sankey>
            )
        }
    }

    export default App;

---

#####See Also#####
- [Customize Labels](/concepts/05%20UI%20Components/Sankey/15%20Node%20Labels/05%20Customize%20Labels.md '/Documentation/Guide/UI_Components/Sankey/Node_Labels/Customize_Labels/')
- [Resolve Label Overlapping](/concepts/05%20UI%20Components/Sankey/15%20Node%20Labels/10%20Resolve%20Overlapping.md '/Documentation/Guide/UI_Components/Sankey/Node_Labels/Resolve_Overlapping/')
- [Sankey API Reference](/api-reference/10%20UI%20Components/dxSankey '/Documentation/ApiReference/UI_Components/dxSankey/')
