# Vue 3.x + vue-plotly
Description: TBD

## Known Issues

### 1. The `vue-plotly` package (v1.1.0) has some incorrect code
- The `package.json` file has some incorrect path references in it:
  - `"module": "dist/vue-plotly.common.min.js"` should refer to `"dist/vue-plotly.common.js"`, there's no minified version of the file in the distributed code...
  - ...But for `"main": "dist/vue-plotly.umd.js"` we have a minified version in the distributed code that should be referred to instead, `"dist/vue-plotly.umd.min.js"`
- It's using the `plotly.js` package instead of the recommended version, `plotly.js-dist`
#### 1.1. Workarounds
- Choose another package to deal with charts on your Vue project
- Use the `plotly.js-dist` package directly, wrapping it with your own Vue component
- Fork the `vue-plotly` repository, make the corrections, publish and use your custom solution
- Use the previous installation in `node_modules` as a basis, make the corrections and rebuild the package locally
