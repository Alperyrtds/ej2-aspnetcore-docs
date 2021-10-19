---
title: "Getting Started(ASP.NET Core)"
component: "Pivot Grid"
description: "Getting started section briefly explains on how to create and add a pivot grid in an application."
---

# Getting Started with ASP.NET Core

> Starting with v16.2.0.x, if you reference Syncfusion assemblies from trial setup or from the NuGet feed, you also have to include a license key in your projects. Please refer to this [link](https://help.syncfusion.com/common/essential-studio/licensing/license-key) to know about registering Syncfusion license key in your ASP.NET Core application to use our components.

## Prerequisites

To get start with ASP.NET Core application, need to ensure the following software to be installed on the machine.
* Visual Studio 2017
* DotNet Core 2.0

## Setup ASP.NET Core application with Essential JS 2 for ASP.NET Core

Follow below steps to create ASP.NET Core Application.

**Step 1:** Create ASP.NET Core Web Application with default template project in Visual Studio 2017.

![Alt text](./images/default-template.png)

**Step 2:** Once your project is created, we need to add Syncfusion EJ2 package into your application using `NuGet Package Manager`.

Follow the below steps to add **Syncfusion EJ2** package in your application.

* Select the "Tools->NuGet Package Manager->Package Manager settings", a dialog window will open.

* Navigate to the "NuGet Package Manager->Package Sources" from the options dialog.

* Click the **Add** button to create the new package sources.

* Select the newly created "Package Source" and rename the source name using the "Name" input box.

    **Name**: Name of the package that listed in "Available package sources".

    **Source**: Syncfusion ASP.NET Core NuGet Package feed URL

![Alt text](./images/package-manager-core.png)

**Step 3:** Once the **Syncfusion EJ2** package is added, open `nuGet` package manager window.

> To open `nuGet` package manager window, right click on the project and select **Manage NuGet Packages** option.

![Alt text](./images/solution-explorer-core.png)

Install the **Syncfusion.EJ2** package to the application

![Alt text](./images/nuget-demo.png)

> Also you will find more details to add Syncfusion EJ2 package to your application [here](../nuget-packages.html).

After installation is completed, it will included in the project. You can refer it in the "Assembly Reference" of your project.

> We need to install **NewtonSoft.JSON** as dependency since it **Syncfusion.EJ2** is dependent to NewtonSoft.JSON package.

## Adding TagHelpers

Open the `Views/_ViewImports.cshtml` file and add the following namespace for **Syncfusion.EJ2** package reference and Tag Helper support.

```cs
@addTagHelper *, Microsoft.AspNetCore.Mvc.TagHelpers
@addTagHelper *, Syncfusion.EJ2
```

## Adding client side resource

Add client side resource through [`CDN`](http://ej2.syncfusion.com/15.4.23/documentation/base/deployment.html?lang=typescript#cdn) or local [`package`](https://www.npmjs.com/package/@syncfusion/ej2) in the layout page **Views/Shared/_Layout.cshtml.**

```html
<head>
@* Syncfusion Essential JS 2 Styles *@
<link rel="stylesheet" href="https://cdn.syncfusion.com/ej2/material.css" />

@* Syncfusion Essential JS 2 Scripts *@
<script src="https://cdn.syncfusion.com/ej2/dist/ej2.min.js"></script>
</head>
```

## Adding ScriptManager

Add the Script Manager reference in the layout page `Views/Shared/_Layout.cshtml`. The Script Manager need to be added after body rendered.

```html
<body>
    @RenderBody()
    @RenderSection("Scripts", required: false)
    <ejs-scripts></ejs-scripts>
</body>
```

## Adding component to the application

Add the below code to your `Index.cshtml` view page which is present under `Views/Home` folder to initialize the pivot grid.

{% aspTab template="pivot-grid/getting-start-core/pivot-grid", sourceFiles="pivotgrid.cs" %}

{% endaspTab %}

## Enable Grouping Bar

The Grouping Bar feature automatically populates fields from the bound data source and allows end users to drag fields between different axes such as columns, rows, values, and filters, and create pivot views at runtime. It can be enabled by setting the `showGroupingBar` property to **true**.

{% aspTab template="pivot-grid/getting-start-core/groupingbar", sourceFiles="groupingbar.cs" %}

{% endaspTab %}

## Enable Pivot Field List

The component provides a built-in Field List similar to Microsoft Excel. It allows you to add or remove fields and also rearrange the fields between different axes, including column, row, value, and filter along with filter and sort options dynamically at runtime. It can be enabled by setting the `showFieldList` property to **true**.

{% aspTab template="pivot-grid/getting-start-core/fieldlist", sourceFiles="fieldlist.cs" %}

{% endaspTab %}

## Calculated field

The calculated field feature allows user to insert or add a new calculated field based on the available fields from the bound data source. It can be customized using the `calculatedFieldsSettings` property through code behind. The setting required for calculate field feature at code behind are:
* `name`: it allows to indicate the given calculated field with unique name.
* `formula`: it allows to set the formula base on the given datasource.

Also calculated fields can be added at run time through the built-in popup. The popup can be enabled by setting the `allowCalculatedField` property to **true**.

> Calculated field is applicable only for value fields.

{% aspTab template="pivot-grid/getting-start-core/calculatedfield", sourceFiles="calculatedfield.cs" %}

{% endaspTab %}

Output be like the below.

![Alt text](./images/pivotgrid-sample.png)