---
id: dxOverlay.Options.onHiding
type: function(e)
default: null
---
---
##### shortDescription
A function that is executed before the UI component is hidden.

##### param(e): Object
Information about the event.

##### field(e.cancel): Boolean
Set this field to **true** if you want the {WidgetName} to remain visible.

##### field(e.component): {WidgetName}
The UI component's instance.

##### field(e.element): DxElement
#include common-ref-elementparam with { element: "UI component" }

##### field(e.model): any
Model data. Available only if Knockout is used.

---
