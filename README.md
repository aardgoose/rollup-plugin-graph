# rollup-plugin-graph

Generates module dependencies graph, using the DOT language. To actually draw images, you will need the `graphviz` toolbox.

In your `rollup.config.js`:
```js
let graph = require("rollup-plugin-graph");
let graphOptions = {prune: true};

module.exports = {
    /* ... */
    plugins: [ graph(graphOptions) ]
};
```

In your terminal:
```sh
rollup -c | dot -Tpng > graph.png
```

## Options

There is only one option available.

  * `prune` (bool) Whether to prune the resulting graph, leaving only cyclic dependencies.
  
