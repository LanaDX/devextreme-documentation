---
id: dxResponsiveBox.Options.screenByWidth
type: function()
default: null
---
---
##### shortDescription
Specifies the function returning the [size qualifier](/concepts/05%20UI%20Components/ResponsiveBox/05%20Size%20Qualifiers.md '/Documentation/Guide/UI_Components/ResponsiveBox/Size_Qualifiers/') depending on the screen's width.

---
The function passed to this property accepts the screen's width as a parameter and should return a string containing the needed size qualifier.

    <!--JavaScript-->
    var responsiveBoxOptions: {
        screenByWidth: function(width) {
            if( width < 768 )
                return "xs";
            if( width < 992 )
                return "sm";
            if( width < 1200 )
                return "md";
            return "lg";
        }
    }