# Wangscape-examples

## Purpose
This repository holds [Wangscape](https://github.com/Wangscape/Wangscape) configurations, which serve several purposes:
* They should demonstrate the range of possibilities of Wangscape's tileset generation.
* They should be alterable to suit different users' tileset requirements.
* They should demonstrate the principles involved in writing Wangscape configurations.

## Remote builds
This repository also has AppVeyor configured to remotely build some example configurations.
For each of these, a map is rendered using the resulting tileset and uploaded as a build artefact.
This can be used to run Wangscape without needing to download or build it.

To take advantage of this, [fork the project](https://github.com/Wangscape/Wangscape-examples#fork-destination-box) to your own Github account,
[log into AppVeyor](https://ci.appveyor.com/login), and add your `Wangscape-examples` fork as a project.
It will then run every time you commit to the `master` branch.

You can choose which configurations are built by altering the `Examples` environment variable in `appveyor.yml`.
The value should be a semicolon-separated list of folders in the `configurations` directory.
For instance, if the current value is `squares;gradient-fade;gradient-dither;zigzag;jagged;wavy-subtle;wavy-bold`,
but you only want to see the results from your own configuration in `configurations/awesome/`, change the value to `awesome`.
The options file at `configurations/awesome/options.json` will be built.

Free AppVeyor accounts allow only 60 minutes before a build is cancelled, so make sure the jobs are not too large.
Don't put too many terrains in a clique, and don't build too many different configurations.

If you want the map to be rendered with a specific terrain grid, provide a file named `fixed_map.json` in the same folder as `options.json`.
It should be formatted like the following:
```json
{
  "size":[2,3],
  "map":[
    ["g","g","g","g"],
    ["c","c","c","c"],
    ["x","x","x","x"],
    ["y","y","y","y"],
    ["z","z","z","z"],
  ]
}
```
N.B. This is still an experimental feature, and we haven't provided any tools for working with this format!

## Contributing
We welcome contributions to this collection. Please see [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines on doing this.
The [contribution guidelines for the main Wangscape repository](https://github.com/Wangscape/Wangscape/blob/master/CONTRIBUTING.md) also apply here.
