# Custom Template Drawer as Side Navigation

This sample project shows one way to use the [Telerik Drawer](https://demos.telerik.com/blazor-ui/drawer/overview) as a side navigation in your project - this sample uses the [Template](https://docs.telerik.com/blazor-ui/components/drawer/templates#template) of the component to implement its out-of-the-box functionality with custom application code (such as item selection, navigation) and to add the expand/collapse button inside the side panel, while still keeping the `@Body` in the `<Content>` so navigation does not affect the drawer.

Key points of interest:

* The Drawers [Template](https://docs.telerik.com/blazor-ui/components/drawer/templates#template) is used in order to control the rendering of the entire component. 

* All the logic, styles and code related to the drawer are in the `~/Shared/MainLayout.razor` file. You should separate them according to your project structure and best practices.

* Code comments in the file provide details.

* CSS rules define the size of the various containers and scrolling:
    * The drawer will take up the entire viewport.
    * Scrolling happens in the content area of the drawer only.
    * The sticky header stays above the content.
    
* The current page is denoted by the selected item in the drawer:
    * On initial load it is taken from the Data collection with the help of the `NavigationManager`.
    * On SPA navigation, the navigation happens in the `@Body` so the click selects the item and it does not dispose it.
    
* In this sample, the list of links is hardcoded for brevity. You can populate it later based on user roles and privileges or any other applicable business logic.