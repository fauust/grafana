---
keywords:
- grafana
- schema
labels:
  products:
  - enterprise
  - oss
title: PieChartPanelCfg kind
---

> Both documentation generation and kinds schemas are in active development and subject to change without prior notice.

## PieChartPanelCfg

#### Maturity: [experimental](../../../maturity/#experimental)

#### Version: 0.0

| Property                | Type                                        | Required | Default | Description                                                                                                                                                                                                                   |
| ----------------------- | ------------------------------------------- | -------- | ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `FieldConfig`           | [HideableFieldConfig](#hideablefieldconfig) | **Yes**  |         | TODO docs                                                                                                                                                                                                                     |
| `Options`               | [object](#options)                          | **Yes**  |         |                                                                                                                                                                                                                               |
| `PieChartLabels`        | string                                      | **Yes**  |         | Select labels to display on the pie chart.<br/> - Name - The series or field name.<br/> - Percent - The percentage of the whole.<br/> - Value - The raw numerical value.<br/>Possible values are: `name`, `value`, `percent`. |
| `PieChartLegendOptions` | [object](#piechartlegendoptions)            | **Yes**  |         |                                                                                                                                                                                                                               |
| `PieChartLegendValues`  | string                                      | **Yes**  |         | Select values to display in the legend.<br/> - Percent: The percentage of the whole.<br/> - Value: The raw numerical value.<br/>Possible values are: `value`, `percent`.                                                      |
| `PieChartType`          | string                                      | **Yes**  |         | Select the pie chart display style.<br/>Possible values are: `pie`, `donut`.                                                                                                                                                  |

### HideableFieldConfig

TODO docs

| Property   | Type                                  | Required | Default | Description |
| ---------- | ------------------------------------- | -------- | ------- | ----------- |
| `hideFrom` | [HideSeriesConfig](#hideseriesconfig) | No       |         | TODO docs   |

### HideSeriesConfig

TODO docs

| Property  | Type    | Required | Default | Description |
| --------- | ------- | -------- | ------- | ----------- |
| `legend`  | boolean | **Yes**  |         |             |
| `tooltip` | boolean | **Yes**  |         |             |
| `viz`     | boolean | **Yes**  |         |             |

### Options

It extends [OptionsWithTooltip](#optionswithtooltip) and [SingleStatBaseOptions](#singlestatbaseoptions).

| Property        | Type                                            | Required | Default | Description                                                                                                                                 |
| --------------- | ----------------------------------------------- | -------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| `displayLabels` | string[]                                        | **Yes**  |         |                                                                                                                                             |
| `legend`        | [PieChartLegendOptions](#piechartlegendoptions) | **Yes**  |         |                                                                                                                                             |
| `pieType`       | string                                          | **Yes**  |         | Select the pie chart display style.<br/>Possible values are: `pie`, `donut`.                                                                |
| `tooltip`       | [VizTooltipOptions](#viztooltipoptions)         | **Yes**  |         | _(Inherited from [OptionsWithTooltip](#optionswithtooltip))_<br/>TODO docs                                                                  |
| `orientation`   | string                                          | No       |         | _(Inherited from [SingleStatBaseOptions](#singlestatbaseoptions))_<br/>TODO docs<br/>Possible values are: `auto`, `vertical`, `horizontal`. |
| `reduceOptions` | [ReduceDataOptions](#reducedataoptions)         | No       |         | _(Inherited from [SingleStatBaseOptions](#singlestatbaseoptions))_<br/>TODO docs                                                            |
| `text`          | [VizTextDisplayOptions](#viztextdisplayoptions) | No       |         | _(Inherited from [SingleStatBaseOptions](#singlestatbaseoptions))_<br/>TODO docs                                                            |

### OptionsWithTooltip

TODO docs

| Property  | Type                                    | Required | Default | Description |
| --------- | --------------------------------------- | -------- | ------- | ----------- |
| `tooltip` | [VizTooltipOptions](#viztooltipoptions) | **Yes**  |         | TODO docs   |

### VizTooltipOptions

TODO docs

| Property | Type   | Required | Default | Description                                                   |
| -------- | ------ | -------- | ------- | ------------------------------------------------------------- |
| `mode`   | string | **Yes**  |         | TODO docs<br/>Possible values are: `single`, `multi`, `none`. |
| `sort`   | string | **Yes**  |         | TODO docs<br/>Possible values are: `asc`, `desc`, `none`.     |

### PieChartLegendOptions

It extends [VizLegendOptions](#vizlegendoptions).

| Property      | Type     | Required | Default | Description                                                                                                                                                                                          |
| ------------- | -------- | -------- | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `calcs`       | string[] | **Yes**  |         | _(Inherited from [VizLegendOptions](#vizlegendoptions))_                                                                                                                                             |
| `displayMode` | string   | **Yes**  |         | _(Inherited from [VizLegendOptions](#vizlegendoptions))_<br/>TODO docs<br/>Note: "hidden" needs to remain as an option for plugins compatibility<br/>Possible values are: `list`, `table`, `hidden`. |
| `placement`   | string   | **Yes**  |         | _(Inherited from [VizLegendOptions](#vizlegendoptions))_<br/>TODO docs<br/>Possible values are: `bottom`, `right`.                                                                                   |
| `showLegend`  | boolean  | **Yes**  |         | _(Inherited from [VizLegendOptions](#vizlegendoptions))_                                                                                                                                             |
| `values`      | string[] | **Yes**  |         |                                                                                                                                                                                                      |
| `asTable`     | boolean  | No       |         | _(Inherited from [VizLegendOptions](#vizlegendoptions))_                                                                                                                                             |
| `isVisible`   | boolean  | No       |         | _(Inherited from [VizLegendOptions](#vizlegendoptions))_                                                                                                                                             |
| `sortBy`      | string   | No       |         | _(Inherited from [VizLegendOptions](#vizlegendoptions))_                                                                                                                                             |
| `sortDesc`    | boolean  | No       |         | _(Inherited from [VizLegendOptions](#vizlegendoptions))_                                                                                                                                             |
| `width`       | number   | No       |         | _(Inherited from [VizLegendOptions](#vizlegendoptions))_                                                                                                                                             |

### VizLegendOptions

TODO docs

| Property      | Type     | Required | Default | Description                                                                                                                             |
| ------------- | -------- | -------- | ------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| `calcs`       | string[] | **Yes**  |         |                                                                                                                                         |
| `displayMode` | string   | **Yes**  |         | TODO docs<br/>Note: "hidden" needs to remain as an option for plugins compatibility<br/>Possible values are: `list`, `table`, `hidden`. |
| `placement`   | string   | **Yes**  |         | TODO docs<br/>Possible values are: `bottom`, `right`.                                                                                   |
| `showLegend`  | boolean  | **Yes**  |         |                                                                                                                                         |
| `asTable`     | boolean  | No       |         |                                                                                                                                         |
| `isVisible`   | boolean  | No       |         |                                                                                                                                         |
| `sortBy`      | string   | No       |         |                                                                                                                                         |
| `sortDesc`    | boolean  | No       |         |                                                                                                                                         |
| `width`       | number   | No       |         |                                                                                                                                         |

### ReduceDataOptions

TODO docs

| Property | Type     | Required | Default | Description                                                  |
| -------- | -------- | -------- | ------- | ------------------------------------------------------------ |
| `calcs`  | string[] | **Yes**  |         | When !values, pick one value for the whole field             |
| `fields` | string   | No       |         | Which fields to show. By default this is only numeric fields |
| `limit`  | number   | No       |         | if showing all values limit                                  |
| `values` | boolean  | No       |         | If true show each row value                                  |

### SingleStatBaseOptions

TODO docs

It extends [OptionsWithTextFormatting](#optionswithtextformatting).

| Property        | Type                                            | Required | Default | Description                                                                              |
| --------------- | ----------------------------------------------- | -------- | ------- | ---------------------------------------------------------------------------------------- |
| `orientation`   | string                                          | **Yes**  |         | TODO docs<br/>Possible values are: `auto`, `vertical`, `horizontal`.                     |
| `reduceOptions` | [ReduceDataOptions](#reducedataoptions)         | **Yes**  |         | TODO docs                                                                                |
| `text`          | [VizTextDisplayOptions](#viztextdisplayoptions) | No       |         | _(Inherited from [OptionsWithTextFormatting](#optionswithtextformatting))_<br/>TODO docs |

### OptionsWithTextFormatting

TODO docs

| Property | Type                                            | Required | Default | Description |
| -------- | ----------------------------------------------- | -------- | ------- | ----------- |
| `text`   | [VizTextDisplayOptions](#viztextdisplayoptions) | No       |         | TODO docs   |

### VizTextDisplayOptions

TODO docs

| Property    | Type   | Required | Default | Description              |
| ----------- | ------ | -------- | ------- | ------------------------ |
| `titleSize` | number | No       |         | Explicit title text size |
| `valueSize` | number | No       |         | Explicit value text size |
