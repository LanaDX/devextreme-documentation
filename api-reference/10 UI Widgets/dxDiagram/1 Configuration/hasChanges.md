---
id: dxDiagram.Options.hasChanges
type: Boolean
default: false
---
---
##### shortDescription
Indicates whether the diagram content has been changed.

---
The **hasChanges** option is set to **true** on any diagram change. You can use this option together with the [optionChanged](/Documentation/ApiReference/UI_Widgets/dxDiagram/Events/#optionChanged) event to implement diagram content autosave.

#####jQuery

    var autoSaveIntervalMs = 2000;
    var autoSaveTimeout = -1;
    $("#diagram").dxDiagram({
    onOptionChanged: function(e) {
        if(e.name === "hasChanges" && e.value && autoSaveTimeout === -1) {
            autoSaveTimeout = setTimeout(function() {
                var data = e.component.export();
                window.localStorage.setItem("foo", data); // store data in some storage
                autoSaveTimeout = -1;
                e.component.option("hasChanges", false);
            }, autoSaveIntervalMs);
        }
    }
    ...  