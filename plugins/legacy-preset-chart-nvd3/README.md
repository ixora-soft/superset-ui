## @superset-ui/legacy-preset-chart-nvd3

[![Version](https://img.shields.io/npm/v/@superset-ui/legacy-preset-chart-nvd3.svg?style=flat-square)](https://www.npmjs.com/package/@superset-ui/legacy-preset-chart-nvd3)
[![David (path)](https://img.shields.io/david/apache-superset/superset-ui-plugins.svg?path=packages%2Fsuperset-ui-legacy-preset-chart-nvd3&style=flat-square)](https://david-dm.org/apache-superset/superset-ui-plugins?path=packages/superset-ui-legacy-preset-chart-nvd3)

This plugin provides Big Number for Superset.

### Usage

Import the preset and register. This will register all the chart plugins under nvd3.

```js
import { NVD3ChartPreset } from '@superset-ui/legacy-preset-chart-nvd3';

new NVD3ChartPreset().register();
```

or register charts one by one. Configure `key`, which can be any `string`, and register the plugin.
This `key` will be used to lookup this chart throughout the app.

```js
import {
  AreaChartPlugin,
  LineChartPlugin,
} from '@superset-ui/legacy-preset-chart-nvd3';

new AreaChartPlugin().configure({ key: 'area' }).register();
new LineChartPlugin().configure({ key: 'line' }).register();
```

Then use it via `SuperChart`. See
[storybook](https://apache-superset.github.io/superset-ui-plugins/?selectedKind=plugin-chart-nvd3)
for more details.

```js
<SuperChart
  chartType="line"
  width={600}
  height={600}
  formData={...}
  queriesData={[{
    data: {...},
  }]}
/>
```
