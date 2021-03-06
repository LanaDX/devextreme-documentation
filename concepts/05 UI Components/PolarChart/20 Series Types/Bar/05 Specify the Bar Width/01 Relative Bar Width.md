Regulating the empty space on a bar's sides controls the relative angular bar width. Use the [barPadding](/api-reference/10%20UI%20Components/dxPolarChart/5%20Series%20Types/CommonPolarChartSeries/barPadding.md '/Documentation/ApiReference/UI_Components/dxPolarChart/Configuration/series/#barPadding') property to specify how much of the available sector should be empty. For example, a **barPadding** of 0.1 leaves 10% of the available sector empty giving the rest to the bar.

---
##### jQuery

    <!--JavaScript-->$(function () {
        $("#polarChartContainer").dxPolarChart({
            series: [{
                // ...
                barPadding: 0.1 // for an individual series
            }, {
                // ...
            }],
            commonSeriesSettings: {
                // ...
                barPadding: 0.1 // for all series in the chart
            }
        });
    });

##### Angular

    <!--HTML-->
    <dx-polar-chart ... >
        <dxi-series
            [barPadding]="0.1"> <!-- for an individual series -->
        </dxi-series>
        <dxi-series ... ></dxi-series>
        ...
        <dxo-common-series-settings
            [barPadding]="0.1"> <!-- for all series in the chart -->
        </dxo-common-series-settings>
    </dx-polar-chart>

    <!--TypeScript-->
    import { DxPolarChartModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxPolarChartModule
        ],
        // ...
    })

##### Vue

    <!-- tab: App.vue -->
    <template> 
        <DxPolarChart ... >
            <DxSeries :bar-padding="0.1"/> <!-- for an individual series -->
            <DxSeries ... />
            ...
            <DxCommonSeriesSettings :bar-padding="0.1"/> <!-- for all series in the chart -->
        </DxPolarChart>
    </template>

    <script>
    import DxPolarChart, {
        DxSeries,
        DxCommonSeriesSettings
    } from 'devextreme-vue/polar-chart';

    export default {
        components: {
            DxPolarChart,
            DxSeries,
            DxCommonSeriesSettings
        }
    }
    </script>

##### React

    <!-- tab: App.js -->
    import React from 'react';
    import PolarChart, {
        Series,
        CommonSeriesSettings
    } from 'devextreme-react/polar-chart';

    class App extends React.Component {
        render() {
            return (
                <PolarChart ... >
                    <Series barPadding={0.1} /> {/* for an individual series */}
                    <Series ... />
                    ...
                    <CommonSeriesSettings barPadding={0.1}/> {/* for all series in the chart */}
                </PolarChart>
            );
        }
    }

    export default App;

---

In single-series charts, the available sector equals the interval between two [major ticks](/concepts/05%20UI%20Components/PolarChart/10%20Visual%20Elements/060%20Axis%20Ticks/01%20Axis%20Ticks.md '/Documentation/Guide/UI_Components/PolarChart/Visual_Elements/#Axis_Ticks'). In multi-series charts, it depends on the number of [bars in the parent group](/concepts/05%20UI%20Components/PolarChart/20%20Series%20Types/Bar/05%20Specify%20the%20Bar%20Width '/Documentation/Guide/UI_Components/PolarChart/Series_Types/#Bar/Specify_the_Bar_Width') and the group's angular width.

The parent group's width can be specified using the [barGroupPadding](/api-reference/10%20UI%20Components/dxPolarChart/1%20Configuration/barGroupPadding.md '/Documentation/ApiReference/UI_Components/dxPolarChart/Configuration/#barGroupPadding') property. It works like **barPadding**, dividing the available sector between the bar group and an empty space. For example, a **barGroupPadding** of 0.2 leaves 20% of the sector empty. The available sector is the interval between two major ticks. Unlike **barPadding**, which can be specified for each series individually, **barGroupPadding** applies to the whole chart.

---
##### jQuery

    <!--JavaScript-->$(function () {
        $("#polarChartContainer").dxPolarChart({
            // ...
            barGroupPadding: 0.2
        });
    });

##### Angular

    <!--HTML-->
    <dx-polar-chart ...
        [barGroupPadding]="0.2">
        <!-- ... -->
    </dx-polar-chart>

    <!--TypeScript-->
    import { DxPolarChartModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxPolarChartModule
        ],
        // ...
    })

##### Vue

    <!-- tab: App.vue -->
    <template> 
        <DxPolarChart ...
            :bar-group-padding="0.2">
        </DxPolarChart>
    </template>

    <script>
    import DxPolarChart from 'devextreme-vue/polar-chart';

    export default {
        components: {
            DxPolarChart
        }
    }
    </script>

##### React

    <!-- tab: App.js -->
    import React from 'react';
    import PolarChart from 'devextreme-react/polar-chart';

    class App extends React.Component {
        render() {
            return (
                <PolarChart ...
                    barGroupPadding={0.2}>
                </PolarChart>
            );
        }
    }

    export default App;

---

The following images illustrate how different **barPadding** and **barGroupPadding** values change a chart's appearance. In this example, all series have the same **barPadding**.

<table class="dx-table">
    <tr>
        <th>barGroupPadding: 0 <br/> barPadding: 0</th>
        <th>barGroupPadding: 0.2 <br/> barPadding: 0</th>
        <th>barGroupPadding: 0.2 <br/> barPadding: 0.1</th>
    </tr>
    <tr>
        <td><img src="/images/ChartJS/polarbarwidth/1.png" /></td>
        <td><img src="/images/ChartJS/polarbarwidth/2.png" /></td>
        <td><img src="/images/ChartJS/polarbarwidth/3.png" /></td>
    </tr>
</table>
