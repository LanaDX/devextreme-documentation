If your dataset excludes non-working days, you can skip them on the axis as well by setting the [workdaysOnly](/api-reference/10%20UI%20Components/dxChart/1%20Configuration/argumentAxis/workdaysOnly.md '/Documentation/ApiReference/UI_Components/dxChart/Configuration/argumentAxis/#workdaysOnly') property to **true**. Use the [workWeek](/api-reference/10%20UI%20Components/dxChart/1%20Configuration/argumentAxis/workWeek.md '/Documentation/ApiReference/UI_Components/dxChart/Configuration/argumentAxis/#workWeek') array to specify which days are workdays. You can also include or exclude specific dates from the axis using the [singleWorkdays](/api-reference/10%20UI%20Components/dxChart/1%20Configuration/argumentAxis/singleWorkdays.md '/Documentation/ApiReference/UI_Components/dxChart/Configuration/argumentAxis/#singleWorkdays') and [holidays](/api-reference/10%20UI%20Components/dxChart/1%20Configuration/argumentAxis/holidays.md '/Documentation/ApiReference/UI_Components/dxChart/Configuration/argumentAxis/#holidays') arrays respectively.

---
##### jQuery

    <!--JavaScript-->$(function() {
        $("#chartContainer").dxChart({
            // ...
            argumentAxis: {
                workdaysOnly: true,
                workWeek: [0, 1, 2, 3, 4, 5],
                holidays: ["2017/1/16", "2017/2/20", "2017/5/29"]
                singleWorkdays: ["2017/1/1"]
            }
        });
    });

##### Angular

    <!--HTML--><dx-chart ... >
        <dxo-argument-axis
            [workdaysOnly]="true"
            [workWeek]="[0, 1, 2, 3, 4, 5]"
            [holidays]="['2017/1/16', '2017/2/20', '2017/5/29']"
            [singleWorkdays]="['2017/1/1']">
        </dxo-argument-axis>
    </dx-chart>

    <!--TypeScript-->
    import { DxChartModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxChartModule
        ],
        // ...
    })

##### Vue

    <!-- tab: App.vue -->
    <template> 
        <DxChart ... >
            <DxArgumentAxis
                :workdays-only="true"
                :work-week="[0, 1, 2, 3, 4, 5]"
                :holidays="['2017/1/16', '2017/2/20', '2017/5/29']"
                :single-workdays="['2017/1/1']"
            />
        </DxChart>
    </template>

    <script>
    import DxChart, {
        DxArgumentAxis
    } from 'devextreme-vue/chart';

    export default {
        components: {
            DxChart,
            DxArgumentAxis
        }
    }
    </script>

##### React

    <!-- tab: App.js -->
    import React from 'react';
    import Chart, {
        ArgumentAxis
    } from 'devextreme-react/chart';

    const workWeek = [0, 1, 2, 3, 4, 5];
    const holidays = ['2017/1/16', '2017/2/20', '2017/5/29'];
    const singleWorkdays = ['2017/1/1'];

    class App extends React.Component {
        render() {
            return (
                <Chart ... >
                    <ArgumentAxis
                        workdaysOnly={true}
                        workWeek={workWeek}
                        holidays={holidays}
                        singleWorkdays={singleWorkdays}
                    />
                </Chart>
            );
        }
    }

    export default App;

---

[note] This feature is available for the argument axis only.

