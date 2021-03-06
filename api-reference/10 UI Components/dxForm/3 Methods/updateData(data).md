---
id: dxForm.updateData(data)
---
---
##### shortDescription
Merges the passed `data` object with [formData](/api-reference/10%20UI%20Components/dxForm/1%20Configuration/formData.md '/Documentation/ApiReference/UI_Components/dxForm/Configuration/#formData'). Matching properties in **formData** are overwritten and new properties added.

##### param(data): Object
Data fields with their new values.

---
[note]

This method does not replace the **formData** object. To replace it, use the [option(optionName, optionValue)](/api-reference/10%20UI%20Components/Component/3%20Methods/option(optionName_optionValue).md '/Documentation/ApiReference/UI_Components/dxForm/Methods/#optionoptionName_optionValue') method as shown below:
    
    <!--JavaScript-->
    formInstance.option("formData", newFormData);

[/note]

#####See Also#####
#include common-link-callmethods