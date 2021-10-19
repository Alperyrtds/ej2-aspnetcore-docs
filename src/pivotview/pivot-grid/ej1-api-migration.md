---
title: "Migration from Essential JS 1"
component: "Pivot Grid"
description: "Explains the common steps for migrating from Essential JS 1 application to Essential JS 2 components especially, pivot grid component."
---

# Migration from Essential JS 1

This article describes the API migration process of Pivot Grid component from Essential JS 1 to Essential JS 2.

## Data Binding

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
| Data source | **property:** dataSource<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-data-source data="@ViewBag.data"></e-data-source>`<br/>`</ej-pivot-grid>`| **property:** dataSource<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource data="@ViewBag.data"></e-datasource>`<br/>`</ejs-pivotview>`|
| Rows |**property:** rows<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-data-source>`<br/>`<e-pivot-rows>`<br/>`<e-row-field field-name="Country" field-caption="Country"></e-row-field>`<br/>`</e-pivot-rows>`<br/>`</e-data-source>`<br/>`</ej-pivot-grid>`| **property:** rows<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource>`<br/>`<e-rows>`<br/>`<e-field name="company" caption= "Industry"></e-field>`<br/>`</e-rows>`<br/>`</e-datasource>`<br/>`</ejs-pivotview>`|
| Columns |**property:** columns<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-data-source>`<br/>`<e-pivot-columns>`<br/>`<e-column-field field-name="Country" field-caption="Country"></e-column-field>`<br/>`</e-pivot-columns>`<br/>`</e-data-source>`<br/>`</ej-pivot-grid>`| **property:** columns<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource>`<br/>`<e-columns>`<br/>`<e-field name="company" caption= "Industry"></e-field>`<br/>`</e-columns>`<br/>`</e-datasource>`<br/>`</ejs-pivotview>`|
| Values |**property:** values<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-data-source>`<br/>`<e-pivot-values>`<br/>`<e-value-field field-name="balance" field-caption="Balance($)"></e-value-field>`<br/>`</e-pivot-values>`<br/>`</e-data-source>`<br/>`</ej-pivot-grid>`| **property:** values<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource>`<br/>`<e-values>`<br/>`<e-field name="balance" caption= "Balance($)"></e-field>`<br/>`</e-values>`<br/>`</e-datasource>`<br/>`</ejs-pivotview>`|
|Filters |**property:** filters<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-data-source>`<br/>`<e-pivot-filters>`<br/>`<e-filter-field field-name="Country" field-caption="Country"></e-filter-field>`<br/>`</e-pivot-filters>`<br/>`</e-data-source>`<br/>`</ej-pivot-grid>`|**property:** filters<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource>`<br/>`<e-filters>`<br/>`<e-field name="company" caption= "Industry"></e-field>`<br/>`</e-filters>`<br/>`</e-datasource>`<br/>`</ejs-pivotview>`|
|Value axis position|Not Applicable|**property:** valueAxis<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource valueAxis="row"></e-datasource>`<br/>`</ejs-pivotview>`|

## Aggregation

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Summary Type|**property:** summaryType<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-data-source>`<br/>`<e-pivot-values>`<br/>`<e-value-field field-name="balance" field-caption="Balance($)" summary-type="Count"></e-value-field>`<br/>`</e-pivot-values>`<br/>`</e-data-source>`<br/>`</ej-pivot-grid>`|**property:** type<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource>`<br/>`<e-values>`<br/>`<e-field name="balance" caption= "Balance($)" type= "Count"></e-field>`<br/>`</e-values>`<br/>`</e-datasource>`<br/>`</ejs-pivotview>`|

## Number Format

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Format settings|**property:** format<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-data-source>`<br/>`<e-pivot-values>`<br/>`<e-value-field field-name="balance" field-caption="Balance($)" format="currency"></e-value-field>`<br/>`</e-pivot-values>`<br/>`</e-data-source>`<br/>`</ej-pivot-grid>`|**property:** formatSettings<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource>`<br/>`<e-formatSettings>`<br/>`<e-field name="balance" format="C0" maximumSignificantDigits="10" minimumSignificantDigits="1" useGrouping="true"></e-field>`<br/>`<e-field name="date" format= "dd/MM/yyyy-hh:mm" type= "date"></e-field>`<br/>`</e-formatSettings>`<br/>`</e-datasource>`<br/>`</ejs-pivotview>`|

## Summary Customization

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Show/hide grand totals|**property:** enableGrandTotal<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-data-source enableGrandTotal="false"></e-data-source>`<br/>`</ej-pivot-grid>`|**property:** showGrandTotals<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource showGrandTotals="false"></e-datasource>`<br/>`</ejs-pivotview>`|
|Show/hide row grand totals|**property:** enableRowGrandTotal<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-data-source enableGrandTotal="false"></e-data-source>`<br/>`</ej-pivot-grid>`|**property:** showRowGrandTotals<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource showRowGrandTotals="false"></e-datasource>`<br/>`</ejs-pivotview>`|
|Show/hide column grand totals|**property:** enableColumnGrandTotal<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-data-source enableGrandTotal="false"></e-data-source>`<br/>`</ej-pivot-grid>`|**property:** showColumnGrandTotals<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource showColumnGrandTotals="false"></e-datasource>`<br/>`</ejs-pivotview>`|
|Show/hide sub-totals|Not Applicable|**property:** showSubTotals<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource showSubTotals="false"></e-datasource>`<br/>`</ejs-pivotview>`|
|Show/hide row sub-totals|Not Applicable|**property:** showRowSubTotals<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource showRowSubTotals="false"></e-datasource>`<br/>`</ejs-pivotview>`|
|Show/hide column sub-totals|Not Applicable|**property:** showColumnSubTotals<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource showColumnSubTotals="false"></e-datasource>`<br/>`</ejs-pivotview>`|
| Show/hide sub-totals for specific field|**property:** showSubTotal<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-data-source>`<br/>`<e-pivot-rows>`<br/>`<e-row-field field-name="Country" show-sub-total="false"></e-row-field>`<br/>`</e-pivot-rows>`<br/>`</e-data-source>`<br/>`</ej-pivot-grid>`| **property:** showSubTotals<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource>`<br/>`<e-rows>`<br/>`<e-field name="company" showSubTotals= "false"></e-field>`<br/>`</e-rows>`<br/>`</e-datasource>`<br/>`</ejs-pivotview>`|

## Drill operation

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Expand All|**property:** enableCollapseByDefault<br/><br/>`<ej-pivot-grid id="PivotGrid" enable-collapse-by-default= "true"></ej-pivot-grid>`|**property:** expandAll<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource expandAll= "false"></e-datasource>`<br/>`</ejs-pivotview>`|
|Drill Up/Down|**property:** collapsedMembers<br/><br/>`<ej-pivot-grid id="PivotGrid" load= "onLoad"></ej-pivot-grid>`<br/><br/>`function onLoad(args) {`<br/>`args.model.collapsedMembers = { Country: ["Canada", "France"] }`<br/>`}`|**property:** drilledMembers<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource>`<br/>`<e-drilledmembers>`<br/>`<e-field name="Country" items="@ViewBag.drilledMembers"></e-field>`<br/>`</e-drilledmembers>`<br/>`</e-datasource>`<br/>`</ejs-pivotview>`|

## Field List

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Show/hide field list pop-up button on pivot grid|Not Applicable|**property:** showFieldList<br/><br/>`<ejs-pivotview id="PivotGrid" showFieldList= "true"></ejs-pivotview>`|
|Defer update|**property:** enableDeferUpdate<br/><br/>`<ej-pivot-grid id="PivotGrid" enable-defer-update= "true"></ej-pivot-grid>`|Not Applicable|
|Control initialization|**component:** PivotSchemaDesigner<br/><br/>`<ej-pivot-schema-designer id="PivotSchemaDesigner"></ej-pivot-schema-designer>`|**component:** PivotFieldListComponent<br/><br/>`<ejs-pivotfieldlist id="PivotFieldList"></ejs-pivotfieldlist>`|
|Render mode|Not Applicable|**property:** renderMode<br/><br/>`<ejs-pivotfieldlist id="PivotFieldList" renderMode= "Fixed"></ejs-pivotfieldlist>`|
|Show/hide calculated field button|Not Applicable|**property:** allowCalculatedField<br/><br/>`<ejs-pivotfieldlist id="PivotFieldList" allowCalculatedField= "true"></ejs-pivotfieldlist>`|
|Show/hide value group button|Not Applicable|**property:** showValuesButton<br/><br/>`<ejs-pivotfieldlist id="PivotFieldList" showValuesButton= "true"></ejs-pivotfieldlist>`|

## Grouping Bar

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Show/hide Grouping bar|**property:** enableGroupingBar<br/><br/>`<ej-pivot-grid id="PivotGrid" enable-grouping-bar= "true"></ej-pivot-grid>`|**property:** showGroupingBar<br/><br/>`<ejs-pivotview id="PivotFieldList" showGroupingBar= "true"></ejs-pivotview>`|
|Grouping Bar Settings|Not Applicable|**property:** groupingBarSettings<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-groupingBarSettings showFilterIcon= "false" showSortIcon= "true" showRemoveIcon= "false"></e-groupingBarSettings>`<br/>`</ejs-pivotview>`|
|Show/hide value group button|Not Applicable|**property:** showValuesButton<br/><br/>`<ejs-pivotview id="PivotGrid" showValuesButton= "true"></ejs-pivotview>`|

## Filtering

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Filter settings|**property:** filterItems<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-data-source>`<br/>`<e-pivot-rows>`<br/>`<e-row-field field-name="Country" field-caption="Country">`<br/>`<e-filter-items filter-type= "exclude" values="@ViewBag.filterItems"></e-filter-items>`<br/>`</e-row-field>`<br/>`</e-pivot-rows>`<br/>`</e-data-source>`<br/>`</ej-pivot-grid>`|**property:** filterSettings<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource>`<br/>`<e-filtersettings>`<br/>`<e-field name="eyeColor" type= "Exclude" items="@ViewBag.filterItems"></e-field>`<br/>`</e-filtersettings>`<br/>`</e-datasource>`<br/>`</ejs-pivotview>`|

## Maximum node limit in member editor

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Max node limit in member editor|**property:** maxNodeLimitInMemberEditor<br/><br/>`<ej-pivot-grid id="PivotGrid" max-node-limit-in-member-editor= "100"></ej-pivot-grid>`|**property:** maxNodeLimitInMemberEditor<br/><br/>`<ejs-pivotview id="PivotGrid" maxNodeLimitInMemberEditor= "100"></ejs-pivotview>`|

## No Data Items

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Show/hide "no data" items|Not Applicable|**property:** showNoDataItems<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource>`<br/>`<e-rows>`<br/>`<e-field name="company" showNoDataItems="true"></e-field>`<br/>`</e-rows>`<br/>`</e-datasource>`<br/>`</ejs-pivotview>`|

## Excel-like filtering

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Label filtering|**property:** enableAdvancedFilter<br/><br/>`<ej-pivot-grid id="PivotGrid" enable-advanced-filter= "true">`<br/>`<e-data-source>`<br/>`<e-pivot-rows>`<br/>`<e-row-field field-name="Country" field-caption="Country">`<br/>`<e-advanced-filters>`<br/>`<e-advanced-filter label-filter-operator = "endsWidth" values= "@ViewBag.filterItems"></e-advanced-filter>`<br/>`</e-advanced-filters>`<br/>`</e-row-field>`<br/>`</e-pivot-rows>`<br/>`</e-data-source>`<br/>`</ej-pivot-grid>`|**property:** allowLabelFilter<br/><br/>`<ejs-pivotview id="PivotGrid" allowLabelFilter= "true">`<br/>`<e-datasource>`<br/>`<e-filtersettings>`<br/>`<e-field name="product" type= "Label" condition= "Between" value1= "e" value2= "v"></e-field>`<br/>`</e-filtersettings>`<br/>`</e-datasource>`<br/>`</ejs-pivotview>`|
|Value filtering|**property:** enableAdvancedFilter<br/><br/>`<ej-pivot-grid id="PivotGrid" enable-advanced-filter= "true">`<br/>`<e-data-source>`<br/>`<e-pivot-rows>`<br/>`<e-row-field field-name="Country" field-caption="Country">`<br/>`<e-advanced-filters>`<br/>`<e-advanced-filter measure= "balance" value-filter-operator = "greaterThan" values= "@ViewBag.filterItems"></e-advanced-filter>`<br/>`</e-advanced-filters>`<br/>`</e-row-field>`<br/>`</e-pivot-rows>`<br/>`</e-data-source>`<br/>`</ej-pivot-grid>`|**property:** allowValueFilter<br/><br/>`<ejs-pivotview id="PivotGrid" allowValueFilter= "true">`<br/>`<e-datasource>`<br/>`<e-filtersettings>`<br/>`<e-field name="product" measure= "quantity" type= "Value" condition= "Between" value1= "3250" value2= "5000"></e-field>`<br/>`</e-filtersettings>`<br/>`</e-datasource>`<br/>`</ejs-pivotview>`|

## Drill Through

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Show/hide drill though feature|**property:** enableDrillThrough<br/><br/>`<ej-pivot-grid id="PivotGrid" enable-drill-through= "true"></ej-pivot-grid>`|**property:** allowDrillThrough<br/><br/>`<ejs-pivotview id="PivotGrid" allowDrillThrough= "true"></ejs-pivotview>`|
|Event Triggers when cell clicked in pivot grid widget|**event:** drillThrough<br/><br/>`<ej-pivot-grid id="PivotGrid" drill-through= "onDrillThrough"></ej-pivot-grid>`<br/><br/>`function onDrillThrough() { }`|**event:** drillThrough<br/><br/>`<ejs-pivotview id="PivotGrid" drillThrough= "onDrillThrough"></ejs-pivotview>`<br/><br/>`function onDrillThrough() { }`|

## Cell Editing

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Edit settings|Not Applicable|**property:** editSettings<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-editSettings></e-editSettings>`<br/>`</ejs-pivotview>`|
|Show/hide cell editing feature|**property:** enableCellEditing<br/><br/>`<ej-pivot-grid id="PivotGrid" enable-cell-editing= "true"></ej-pivot-grid>`|**property:** allowEditing<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-editSettings allowAdding="true" allowDeleting="true" allowEditing="true" mode="Dialog"></e-editSettings>`<br/>`</ejs-pivotview>`|

## Hyperlink

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Hyperlink settings|**property:** hyperlink<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-hyperlink></e-hyperlink>`<br/>`</ej-pivot-grid>`|**property:** hyperlinkSettings<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-hyperlinkSettings></e-hyperlinkSettings>`<br/>`</ejs-pivotview>`|
|Show/hide hyperlink to all cells|Not Applicable|**property:** showHyperlink<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-hyperlinkSettings showHyperlink="true"></e-hyperlinkSettings>`<br/>`</ejs-pivotview>`|
|Show/hide hyperlink to row headers|**property:** enableRowHeaderHyperlink<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-hyperlink enable-row-header-hyperlink="true"></e-hyperlink>`<br/>`</ej-pivot-grid>`|**property:** showRowHeaderHyperlink<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-hyperlinkSettings showRowHeaderHyperlink="true"></e-hyperlinkSettings>`<br/>`</ejs-pivotview>`|
|Show/hide hyperlink to column headers|**property:** enableColumnHeaderHyperlink<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-hyperlink enable-column-header-hyperlink="true"></e-hyperlink>`<br/>`</ej-pivot-grid>`|**property:** showColumnHeaderHyperlink<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-hyperlinkSettings showColumnHeaderHyperlink="true"></e-hyperlinkSettings>`<br/>`</ejs-pivotview>`|
|Show/hide hyperlink to value cells|**property:** enableValueCellHyperlink<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-hyperlink enable-value-cell-hyperlink="true"></e-hyperlink>`<br/>`</ej-pivot-grid>`|**property:** showValueCellHyperlink<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-hyperlinkSettings showValueCellHyperlink="true"></e-hyperlinkSettings>`<br/>`</ejs-pivotview>`|
|Show/hide hyperlink to summary cells|**property:** enableSummaryCellHyperlink<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-hyperlink enable-summary-cell-hyperlink="true"></e-hyperlink>`<br/>`</ej-pivot-grid>`|**property:** showSummaryCellHyperlink<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-hyperlinkSettings showSummaryCellHyperlink="true"></e-hyperlinkSettings>`<br/>`</ejs-pivotview>`|
|Show/hide hyperlink using specific conditions|Not Applicable|**property:** conditionalSettings<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-hyperlinkSettings>`<br/>`<e-conditionalsettings>`<br/>`<e-format measure="Sold" conditions="Between" value1="150" value2="200"></e-format>`<br/>`</e-conditionalsettings>`<br/>`</e-hyperlinkSettings>`<br/>`</ejs-pivotview>`|
|Show/hide hyperlink for row or column|Not Applicable|**property:** headerText<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-hyperlinkSettings headerText: 'FY 2015.Q1.Units Sold'></e-hyperlinkSettings>`<br/>`</ejs-pivotview>`|
|Event Triggers when row headers clicked in pivot grid widget|**event:** rowHeaderHyperlinkClick<br/><br/>`<ej-pivot-grid id="PivotGrid" row-header-hyperlink-click= "onClick"></ej-pivot-grid>`<br/><br/>`function onClick() { }`|**event:** hyperlinkCellClick<br/><br/>`<ejs-pivotview id="PivotGrid" hyperlinkCellClick= "onClick"></ejs-pivotview>`<br/><br/>`function onClick() { }`|
|Event Triggers when column headers clicked in pivot grid widget|**event:** columnHeaderHyperlinkClick<br/><br/>`<ej-pivot-grid id="PivotGrid" column-header-hyperlink-click= "onClick"></ej-pivot-grid>`<br/><br/>`function onClick() { }`|**event:** hyperlinkCellClick<br/><br/>`<ejs-pivotview id="PivotGrid" hyperlinkCellClick= "onClick"></ejs-pivotview>`<br/><br/>`function onClick() { }`|
|Event Triggers when value cells clicked in pivot grid widget|**event:** valueCellHyperlinkClick<br/><br/>`<ej-pivot-grid id="PivotGrid" value-cell-hyperlink-click= "onClick"></ej-pivot-grid>`<br/><br/>`function onClick() { }`|**event:** hyperlinkCellClick<br/><br/>`<ejs-pivotview id="PivotGrid" hyperlinkCellClick= "onClick"></ejs-pivotview>`<br/><br/>`function onClick() { }`|
|Event Triggers when summary cells clicked in pivot grid widget|**event:** summaryCellHyperlinkClick<br/><br/>`<ej-pivot-grid id="PivotGrid" summary-cell-hyperlink-click= "onClick"></ej-pivot-grid>`<br/><br/>`function onClick() { }`|**event:** hyperlinkCellClick<br/><br/>`<ejs-pivotview id="PivotGrid" hyperlinkCellClick= "onClick"></ejs-pivotview>`<br/><br/>`function onClick() { }`|

## Defer Layout Update

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Show/hide defer layout update|**property:** enableDeferUpdate<br/><br/>`<ej-pivot-grid id="PivotGrid" enable-defer-update= "true"></ej-pivot-grid>`|**property:** allowDeferLayoutUpdate<br/><br/>`<ejs-pivotview id="PivotGrid" allowDeferLayoutUpdate= "true"></ejs-pivotview>`|

## Sorting

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Enable/disable sorting|Not Applicable|**property:** enableSorting<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource enableSorting= "false"></e-datasource>`<br/>`</ejs-pivotview>`|
|Sort settings|**property:** sortOrder<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-data-source>`<br/>`<e-pivot-rows>`<br/>`<e-row-field field-name="Country" field-caption="Country" sort-order= SortOrder.Descending></e-row-field>`<br/>`</e-pivot-rows>`<br/>`</e-data-source>`<br/>`</ej-pivot-grid>`|**property:** sortSettings<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource>`<br/>`<e-sortSettings>`<br/>`<e-field name="company" order= "Descending"></e-field>`<br/>`</e-sortSettings>`<br/>`</e-datasource>`<br/>`</ejs-pivotview>`|

## Value Sorting

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Enable/disable value sorting|Not Applicable|**property:** enableSorting<br/><br/>`<ejs-pivotview id="PivotGrid" enableValueSorting= "true"></ejs-pivotview>`|
|Value sort settings|**property:** valueSortSettings<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-value-sort header-text= "Bike##Quantity" header-delimiters= "##" sort-order= SortOrder.Descending></e-value-sort>`<br/>`</ej-pivot-grid>`|**property:** valueSortSettings<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource>`<br/>`<e-valuesortsettings headerText= "FY 2015##Sold Amount" headerDelimiter= "##" sortOrder= "Descending"></e-valuesortsettings>`<br/>`</e-datasource>`<br/>`</ejs-pivotview>`|

## Calculated Field

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Show/hide calculated field|Not Applicable|**property:** allowCalculatedField<br/><br/>`<ejs-pivotview id="PivotGrid" allowCalculatedField= "true"></ejs-pivotview>`|
|Calculated field settings|**property:** values<br/><br/>`<ej-pivot-grid id="PivotGrid">`<br/>`<e-data-source>`<br/>`<e-pivot-values>`<br/>`<e-value-field field-name="Amount" field-caption="Amount"></e-value-field>`<br/>`<e-pivot-values>`<br/>`<e-value-field field-name="Price" field-caption="Price" is-calculated-field= "true" formula= "Amount*15"></e-value-field>`<br/>`</e-pivot-values>`<br/>`</e-data-source>`<br/>`</ej-pivot-grid>`|**property:** calculatedFieldSettings<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource>`<br/>`<e-values>`<br/>`<e-field name="Total" type= "CalculatedField"></e-field>`<br/>`</e-calculatedfieldsettings>`<br/>`<e-calculatedfieldsettings>`<br/>`<e-field name="Total" formula: "@totalPrice"></e-field>`<br/>`</e-calculatedfieldsettings>`<br/>`</e-datasource>`<br/>`</ejs-pivotview>`<br/><br/>`@{var stock = "\"" + "Sum(In_Stock)" + "\"";}`<br/>`@{var sold = "\"" + "Sum(Sold)" + "\"";}`<br/>`@{ var totalPrice = stock + "+" + sold;}`|

## Paging

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Paging|**property:** enablePaging<br/><br/>`<ej-pivot-grid id="PivotGrid" enable-paging= "true"></ej-pivot-grid>`|Not Applicable|
|Virtual scrolling|**property:** enableVirtualScrolling<br/><br/>`<ej-pivot-grid id="PivotGrid" enable-virtual-scrolling= "true"></ej-pivot-grid>`|**property:** enableVirtualization<br/><br/>`<ejs-pivotview id="PivotGrid" enableVirtualization= "true"></ejs-pivotview>`|

## Conditional Formatting

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Show/hide conditional formatting|**property:** enableConditionalFormatting<br/><br/>`<ej-pivot-grid id="PivotGrid" enable-conditional-formatting= "true"></ej-pivot-grid>`|**property:** allowConditionalFormatting<br/><br/>`<ejs-pivotview id="PivotGrid" allowConditionalFormatting= "true"></ejs-pivotview>`|
|Conditional formatting settings|**property:** conditionalFormatSettings<br/><br/>`<ej-pivot-grid id="PivotGrid" load= "onLoad"></ej-pivot-grid>`<br/><br/>`function onLoad(args) {`<br/>`args.model.dataSource.conditionalFormatSettings = [{`<br/>`name: "Format2",`<br/> `style: {` <br/>`"color": "#000000",`<br/> `"backgroundcolor": "#0000FF",`<br/> `"bordercolor": "#000000",`<br/>`"borderstyle": "Dashed",`<br/> `"borderwidth": "5",`<br/> `"fontsize": "12",`<br/> `"fontstyle": "Algerian" },`<br/>`condition: ej.PivotGrid.ConditionalOptions.LessThan,`<br/> `value: "200",`<br/> `measures: "Amount,Quantity" }]`<br/>`}`|**property:** conditionalFormatSettings<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-datasource>`<br/>`<e-conditionalformatsettings>`<br/>`<e-format measure= "In Stock" value1= 5000 conditions= "LessThan">`<br/>`<e-style backgroundColor= "#80cbc4" color= "black" fontFamily= "Tahoma" fontSize= "12px"></e-style>`<br/>`</e-format>`<br/>`</e-conditionalformatsettings>`<br/>`</e-datasource>`<br/>`</ejs-pivotview>`|

## Exporting

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Excel Export|Not Applicable|**property:** allowExcelExport<br/><br/>`<ejs-pivotview id="PivotGrid" allowExcelExport= "true"></ejs-pivotview>`|
|Pdf Export|Not Applicable|**property:** allowPdfExport<br/><br/>`<ejs-pivotview id="PivotGrid" allowPdfExport= "true"></ejs-pivotview>`|

## Grid Customization

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Set width for pivot grid|Not Applicable|**property:** width<br/><br/>`<ejs-pivotview id="PivotGrid" width= 800></ejs-pivotview>`|
|Set height for pivot grid|Not Applicable|**property:** height<br/><br/>`<ejs-pivotview id="PivotGrid" height= 400></ejs-pivotview>`|
|Set row height for pivot grid|Not Applicable|**property:** rowHeight<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-gridSettings rowHeight= 60></e-gridSettings>`<br/>`</ejs-pivotview>`|
|Set column width for pivot grid|Not Applicable|**property:** columnWidth<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-gridSettings columnWidth= 120></e-gridSettings>`<br/>`</ejs-pivotview>`|
|Drag and drop column headers in pivot grid|Not Applicable|**property:** allowReordering<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-gridSettings allowReordering= "true"></e-gridSettings>`<br/>`</ejs-pivotview>`|
|Resizing the column headers in pivot grid|**property:** enableColumnResizing<br/><br/>`<ej-pivot-grid id="PivotGrid" enable-column-resizing= "true"></ej-pivot-grid>`|**property:** allowResizing<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-gridSettings allowResizing= "true"></e-gridSettings>`<br/>`</ejs-pivotview>`|
|Wrap the cell content in pivot grid|Not Applicable|**property:** allowTextWrap<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-gridSettings allowTextWrap= "true"></e-gridSettings>`<br/>`</ejs-pivotview>`|
|Display cell border in pivot grid|Not Applicable|**property:** gridLines<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-gridSettings gridLines= "Vertical"></e-gridSettings>`<br/>`</ejs-pivotview>`|
|Cell selection|**property:** enableCellSelection<br/><br/>`<ej-pivot-grid id="PivotGrid" enable-cell-selection= "true"></ej-pivot-grid>`|**property:** allowSelection<br/><br/>`<ejs-pivotview id="PivotGrid" load= "onLoad">`<br/>`<e-gridSettings allowSelection= "true"></e-gridSettings>`<br/>`</ejs-pivotview>`<br/><br/>`function onLoad()  {`<br/>`pivotGridObj = document.getElementById('PivotGrid').ej2_instances[0];`<br/>`pivotGridObj.gridSettings.selectionSettings = {`<br/>`cellSelectionMode: 'Box',`<br/>`type: 'Multiple',`<br/> `mode: 'Cell' };`<br/>`}`|
|Display overflow cell content in pivot grid|Not Applicable|**property:** clipMode<br/><br/>`<ejs-pivotview id="PivotGrid">`<br/>`<e-gridSettings clipMode= "Clip"></e-gridSettings>`<br/>`</ejs-pivotview>`|
|Cell Editing|**property:** enableCellEditing<br/><br/>`<ej-pivot-grid id="PivotGrid" enable-cell-editing= "true"></ej-pivot-grid>`|Not Applicable|
|Cell double click|**property:** enableCellDoubleClick<br/><br/>`<ej-pivot-grid id="PivotGrid" enable-cell-double-click= "true"></ej-pivot-grid>`|Not Applicable|
|Cell context|**property:** enableCellContext<br/><br/>`<ej-pivot-grid id="PivotGrid" enable-cell-context= "true"></ej-pivot-grid>`|Not Applicable|

## Accessibility

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Localization|**property:** locale<br/><br/>`<ej-pivot-grid id="PivotGrid" locale= "es-ES"></ej-pivot-grid>`|**property:** locale<br/><br/>`<ejs-pivotview id="PivotGrid" locale= "es-ES"></ejs-pivotview>`|
|Right to left|**property:** enableRTL<br/><br/>`<ej-pivot-grid id="PivotGrid" enable-rtl= "true"></ej-pivot-grid>`|**property:** enableRtl<br/><br/>`<ejs-pivotview id="PivotGrid" enableRTL= "true"></ejs-pivotview>`|

## Common

| **Behavior** | **API in Essential JS 1** | **API in Essential JS 2** |
| --- | --- | --- |
|Adding custom class to wrapper element|**property:** cssClass<br/><br/>`<ej-pivot-grid id="PivotGrid" css-class= "custom-class"></ej-pivot-grid>`|**property:** cssClass<br/><br/>`<ejs-pivotview id="PivotGrid" cssClass= "custom-class"></ejs-pivotview>`|
|Keeping the model values in cookies|Not Applicable|**property:** enablePersistence<br/><br/>`<ejs-pivotview id="PivotGrid" enablePersistence= "true"></ejs-pivotview>`|
|Event triggers when control initializing|**event:** load<br/><br/>`<ej-pivot-grid id="PivotGrid" load= "onLoad"></ej-pivot-grid>`<br/><br/>`function onLoad() { }`|**event:** load<br/><br/>`<ejs-pivotview id="PivotGrid" load= "onLoad"></ejs-pivotview>`<br/><br/>`function onLoad() { }`|
|Event Triggers before the pivot engine starts|**event:** beforePivotEnginePopulate<br/><br/>`<ej-pivot-grid id="PivotGrid" before-pivot-engine-populate= "onBeforePivotEnginePopulate"></ej-pivot-grid>`<br/><br/>`function onBeforePivotEnginePopulate() { }`|**event:** enginePopulating<br/><br/>`<ejs-pivotview id="PivotGrid" enginePopulating= "onEnginePopulating"></ejs-pivotview>`<br/><br/>`function onEnginePopulating() { }`|
|Event Triggers after the pivot engine populated|**event:** afterPivotEnginePopulate<br/><br/>`<ej-pivot-grid id="PivotGrid" after-pivot-engine-populate= "onAfterPivotEnginePopulate"></ej-pivot-grid>`<br/><br/>`function onAfterPivotEnginePopulate() { }`|**event:** enginePopulated<br/><br/>`<ejs-pivotview id="PivotGrid" enginePopulated= "onEnginePopulated"></ejs-pivotview>`<br/><br/>`function onEnginePopulated() { }`|
|Event Triggers after the control populated with data source|**event:** renderSuccess<br/><br/>`<ej-pivot-grid id="PivotGrid" render-success= "onRenderSuccess"></ej-pivot-grid>`<br/><br/>`function onRenderSuccess() { }`|**event:** dataBound<br/><br/>`<ejs-pivotview id="PivotGrid" dataBound= "onDataBound"></ejs-pivotview>`<br/><br/>`function onDataBound() { }`|
|Event Triggers after the control created|Not Applicable|**event:** created<br/><br/>`<ejs-pivotview id="PivotGrid" created= "onCreated"></ejs-pivotview>`<br/><br/>`function onCreated() { }`|
|Event Triggers when destroy the control|Not Applicable|**event:** destroyed<br/><br/>`<ejs-pivotview id="PivotGrid" destroyed= "onDestroyed"></ejs-pivotview>`<br/><br/>`function onDestroyed() { }`|
|Event Triggers the cell clicked in pivot grid widget|**event:** cellClick<br/><br/>`<ej-pivot-grid id="PivotGrid" cell-click= "onCellClick"></ej-pivot-grid>`<br/><br/>`function onCellClick() { }`|**event:** cellClick<br/><br/>`<ejs-pivotview id="PivotGrid" cellClick= "onCellClick"></ejs-pivotview>`<br/><br/>`function onCellClick() { }`|
