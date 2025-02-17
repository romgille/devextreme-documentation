To specify when the Popover should be shown and hidden, set the [showEvent](/api-reference/10%20UI%20Components/dxPopover/1%20Configuration/showEvent '/Documentation/ApiReference/UI_Components/dxPopover/Configuration/showEvent/') and [hideEvent](/api-reference/10%20UI%20Components/dxPopover/1%20Configuration/hideEvent '/Documentation/ApiReference/UI_Components/dxPopover/Configuration/hideEvent/') properties. These properties can accept several events at once as well as an object.

---
##### jQuery 

    <!--JavaScript-->$(function() {
        $("#popoverContainer").dxPopover({
            target: "#image",
            showEvent: 'dxhoverstart',
            hideEvent: 'dxhoverend'
        });
    });

    <!--HTML--><img id="image" src="https://url/to/an/image" />
    <div id="popoverContainer">
        <p>Popover content</p>
    </div>

##### Angular

    <!--HTML-->
    <img id="image" src="https://url/to/an/image" />
    <dx-popover
        target="#image"
        showEvent="dxhoverstart"
        hideEvent="dxhoverend">
        <div *dxTemplate="let data of 'content'">
            <p>Popover content</p>
        </div>
    </dx-popover>

    <!--TypeScript-->
    import { DxPopoverModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxPopoverModule
        ],
        // ...
    })

##### Vue

    <template>
        <div>
            <img id="image" src="https://url/to/an/image" />
            <DxPopover 
                target="#image"
                show-event="dxhoverstart"
                hide-event="dxhoverend">
                <template>
                    <p>Popover content</p>
                </template>
            </DxPopover>
        </div>
    </template>

    <script>
    import 'devextreme/dist/css/dx.light.css';

    import { DxPopover } from 'devextreme-vue/popover';

    export default {
        components: {
            DxPopover
        }
    }
    </script>

##### React

    import React from 'react';
    import 'devextreme/dist/css/dx.light.css';

    import { Popover } from 'devextreme-react/popover';

    const renderContent = () => {
        return (
            <p>Popover content</p>
        );
    };

    class App extends React.Component {
        render() {
            return (
                <div>
                    <img id="image" src="https://url/to/an/image" />
                    <Popover
                        target="#image"
                        showEvent="dxhoverstart"
                        hideEvent="dxhoverend"
                        contentRender={renderContent}
                    />
                </div>
            );
        }
    }

    export default App;

##### ASP.NET MVC Controls

    <!--Razor C#-->
    @(Html.DevExtreme().Popover()
        .Target("#image")
        .ShowEvent("dxhoverstart")
        .HideEvent("dxhoverend")
        .ContentTemplate(@<text>
            <p>Popover content</p>
        </text>)
    )
    <img id="image" src="https://url/to/an/image" />

---

#include common-demobutton with {
    url: "https://js.devexpress.com/Demos/WidgetsGallery/Demo/Popover/Overview/"
}

The Popover can also be hidden when a user clicks outside it. To control this behavior of the Popover, use the [hideOnOutsideClick](/api-reference/10%20UI%20Components/dxPopover/1%20Configuration/hideOnOutsideClick.md '/Documentation/ApiReference/UI_Components/dxPopover/Configuration/#hideOnOutsideClick') property.

---
##### jQuery 

    <!--JavaScript-->$(function() {
        $("#popoverContainer").dxPopover({
            target: "#image",
            showEvent: 'dxhoverstart',
            hideEvent: 'dxhoverend',
            hideOnOutsideClick: false
        });
    });

    <!--HTML--><img id="image" src="https://url/to/an/image" />
    <div id="popoverContainer">
        <p>Popover content</p>
    </div>

##### Angular

    <!--HTML-->
    <img id="image" src="https://url/to/an/image" />
    <dx-popover
        target="#image"
        showEvent="dxhoverstart"
        hideEvent="dxhoverend"
        [hideOnOutsideClick]="false">
        <div *dxTemplate="let data of 'content'">
            <p>Popover content</p>
        </div>
    </dx-popover>

    <!--TypeScript-->
    import { DxPopoverModule } from "devextreme-angular";
    // ...
    export class AppComponent {
        // ...
    }
    @NgModule({
        imports: [
            // ...
            DxPopoverModule
        ],
        // ...
    })

##### Vue

    <template>
        <div>
            <img id="image" src="https://url/to/an/image" />
            <DxPopover 
                target="#image"
                show-event="dxhoverstart"
                hide-event="dxhoverend"
                :hide-on-outside-click="false">
                <template>
                    <p>Popover content</p>
                </template>
            </DxPopover>
        </div>
    </template>

    <script>
    import 'devextreme/dist/css/dx.light.css';

    import { DxPopover } from 'devextreme-vue/popover';

    export default {
        components: {
            DxPopover
        }
    }
    </script>

##### React

    import React from 'react';
    import 'devextreme/dist/css/dx.light.css';

    import { Popover } from 'devextreme-react/popover';

    const renderContent = () => {
        return (
            <p>Popover content</p>
        );
    };

    class App extends React.Component {
        render() {
            return (
                <div>
                    <img id="image" src="https://url/to/an/image" />
                    <Popover
                        target="#image"
                        showEvent="dxhoverstart"
                        hideEvent="dxhoverend"
                        contentRender={renderContent}
                        hideOnOutsideClick={false}
                    />
                </div>
            );
        }
    }

    export default App;

##### ASP.NET MVC Controls

    <!--Razor C#-->
    @(Html.DevExtreme().Popover()
        .Target("#image")
        .ShowEvent("dxhoverstart")
        .HideEvent("dxhoverend")
        .ContentTemplate(@<text>
            <p>Popover content</p>
        </text>)
        .HideOnOutsideClick(false)
    )
    <img id="image" src="https://url/to/an/image" />

---