To call a widget method, you can apply techniques described in the [Call Methods](/Documentation/Guide/Getting_Started/Widget_Basics_-_jQuery/Call_Methods) topic for jQuery.

As an alternative, you can save the widget instance in a view model property once the widget is initialized...

    <!--JavaScript-->var viewModel = {
        menuInstance: {},
        menuOptions: {
            // ...
            onInitialized: function (e) {
                viewModel.menuInstance = e.component;    
            }
        }
	};

	ko.applyBindings(viewModel);

... and call any method of the saved instance afterwards.

    <!--JavaScript-->viewModel.menuInstance.repaint();

#####See Also#####
- **API Reference**.**WidgetName**.**Methods**, for example, **API Reference**.[Menu](/api-reference/10%20UI%20Widgets/dxMenu '/Documentation/ApiReference/UI_Widgets/dxMenu/').[Methods](/api-reference/10%20UI%20Widgets/dxMenuBase/3%20Methods '/Documentation/ApiReference/UI_Widgets/dxMenu/Methods/')

[tags]basics, knockout, call methods, widget instance