In the closed state, the navigation menu is partially visible because it displays item icons. If the items do not have icons, you can hide the menu. To do this, open the `SideNavOuterToolbar` or `SideNavInnerToolbar` component (depending on the used [layout](/concepts/55%20Vue%20Components/50%20Application%20Template/10%20Layouts.md '/Documentation/Guide/Vue_Components/Application_Template/#Layouts')) and change the `drawerOptions()` computed property as follows:

    <!-- tab: side-nav-outer-toolbar.vue -->
    // ...
    <script>
    // ...
    export default {
        // ...
        computed: {
            drawerOptions() {
                // ...
                return {
                    // ...
                    minMenuSize: 0
                };
            },
            // ...
        },
        // ...
    };
    </script>