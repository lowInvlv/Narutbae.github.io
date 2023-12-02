# Integrating with Build Tools

## Babel {#babel style="position:relative;"}

### Install {#install style="position:relative;"}

``` {data-language="shell"}
npm install @babel/cli @babel/core @babel/preset-typescript --save-dev
```

### .babelrc {#babelrc style="position:relative;"}

```js
{
  "presets": ["@babel/preset-typescript"]
}
```

### Using Command Line Interface {#using-command-line-interface style="position:relative;"}

``` {data-language="shell"}
./node_modules/.bin/babel --out-file bundle.js src/index.ts
```

### package.json {#packagejson style="position:relative;"}

```js
{
  "scripts": {
    "build": "babel --out-file bundle.js main.ts"
  },
}
```

### Execute Babel from the command line {#execute-babel-from-the-command-line style="position:relative;"}

``` {data-language="shell"}
npm run build
```

## Browserify {#browserify style="position:relative;"}

### Install {#install-1 style="position:relative;"}

``` {data-language="shell"}
npm install tsify
```

### Using Command Line Interface {#using-command-line-interface-1 style="position:relative;"}

``` {data-language="shell"}
browserify main.ts -p [ tsify --noImplicitAny ] > bundle.js
```

### Using API {#using-api style="position:relative;"}

```js
var browserify = require("browserify");
var tsify = require("tsify");

browserify()
  .add("main.ts")
  .plugin("tsify", { noImplicitAny: true })
  .bundle()
  .pipe(process.stdout);
```

More details: [smrq/tsify](https://github.com/smrq/tsify)

## Grunt {#grunt style="position:relative;"}

### Install {#install-2 style="position:relative;"}

``` {data-language="shell"}
npm install grunt-ts
```

### Basic Gruntfile.js {#basic-gruntfilejs style="position:relative;"}

```js
module.exports = function (grunt) {
  grunt.initConfig({
    ts: {
      default: {
        src: ["**/*.ts", "!node_modules/**/*.ts"],
      },
    },
  });
  grunt.loadNpmTasks("grunt-ts");
  grunt.registerTask("default", ["ts"]);
};
```

More details:
[TypeStrong/grunt-ts](https://github.com/TypeStrong/grunt-ts)

## Gulp {#gulp style="position:relative;"}

### Install {#install-3 style="position:relative;"}

``` {data-language="shell"}
npm install gulp-typescript
```

### Basic gulpfile.js {#basic-gulpfilejs style="position:relative;"}

```js
var gulp = require("gulp");
var ts = require("gulp-typescript");

gulp.task("default", function () {
  var tsResult = gulp.src("src/*.ts").pipe(
    ts({
      noImplicitAny: true,
      out: "output.js",
    })
  );
  return tsResult.js.pipe(gulp.dest("built/local"));
});
```

More details:
[ivogabe/gulp-typescript](https://github.com/ivogabe/gulp-typescript)

## Jspm {#jspm style="position:relative;"}

### Install {#install-4 style="position:relative;"}

``` {data-language="shell"}
npm install -g jspm@beta
```

*Note: Currently TypeScript support in jspm is in 0.16beta*

More details:
[TypeScriptSamples/jspm](https://github.com/Microsoft/TypeScriptSamples/tree/master/jspm)

## MSBuild {#msbuild style="position:relative;"}

Update project file to include locally installed
`Microsoft.TypeScript.Default.props` (at the top) and
`Microsoft.TypeScript.targets` (at the bottom) files:

``` {data-language="xml"}
<?xml version="1.0" encoding="utf-8"?>
<Project ToolsVersion="4.0" DefaultTargets="Build" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  <!-- Include default props at the top -->
  <Import
      Project="$(MSBuildExtensionsPath32)\Microsoft\VisualStudio\v$(VisualStudioVersion)\TypeScript\Microsoft.TypeScript.Default.props"
      Condition="Exists('$(MSBuildExtensionsPath32)\Microsoft\VisualStudio\v$(VisualStudioVersion)\TypeScript\Microsoft.TypeScript.Default.props')" />

  <!-- TypeScript configurations go here -->
  <PropertyGroup Condition="'$(Configuration)' == 'Debug'">
    <TypeScriptRemoveComments>false</TypeScriptRemoveComments>
    <TypeScriptSourceMap>true</TypeScriptSourceMap>
  </PropertyGroup>
  <PropertyGroup Condition="'$(Configuration)' == 'Release'">
    <TypeScriptRemoveComments>true</TypeScriptRemoveComments>
    <TypeScriptSourceMap>false</TypeScriptSourceMap>
  </PropertyGroup>

  <!-- Include default targets at the bottom -->
  <Import
      Project="$(MSBuildExtensionsPath32)\Microsoft\VisualStudio\v$(VisualStudioVersion)\TypeScript\Microsoft.TypeScript.targets"
      Condition="Exists('$(MSBuildExtensionsPath32)\Microsoft\VisualStudio\v$(VisualStudioVersion)\TypeScript\Microsoft.TypeScript.targets')" />
</Project>
```

More details about defining MSBuild compiler options: [Setting Compiler
Options in MSBuild projects](compiler-options-in-msbuild)

## NuGet {#nuget style="position:relative;"}

-   Right-Click -\> Manage NuGet Packages
-   Search for `Microsoft.TypeScript.MSBuild`
-   Hit `Install`
-   When install is complete, rebuild!

More details can be found at [Package Manager
Dialog](http://docs.nuget.org/Consume/Package-Manager-Dialog) and [using
nightly builds with
NuGet](https://github.com/Microsoft/TypeScript/wiki/Nightly-drops#using-nuget-with-msbuild)

## Rollup {#rollup style="position:relative;"}

### Install {#install-5 style="position:relative;"}

``` {data-language="typescript"}
npm install @rollup/plugin-typescript --save-dev
```

Note that both `typescript` and `tslib` are peer dependencies of this
plugin that need to be installed separately.

### Usage {#usage style="position:relative;"}

Create a `rollup.config.js` [configuration
file](https://www.rollupjs.org/guide/en/#configuration-files) and import
the plugin:

```js
// rollup.config.js
import typescript from '@rollup/plugin-typescript';

export default {
  input: 'src/index.ts',
  output: {
    dir: 'output',
    format: 'cjs'
  },
  plugins: [typescript()]
};
```

## Svelte Compiler {#svelte-compiler style="position:relative;"}

### Install {#install-6 style="position:relative;"}

``` {data-language="typescript"}
npm install --save-dev svelte-preprocess
```

Note that `typescript` is an optional peer dependencies of this plugin
and needs to be installed separately. `tslib` is not provided either.

You may also consider
[`svelte-check`](https://www.npmjs.com/package/svelte-check) for CLI
type checking.

### Usage {#usage-1 style="position:relative;"}

Create a `svelte.config.js` configuration file and import the plugin:

```js
// svelte.config.js
import preprocess from 'svelte-preprocess';

const config = {
  // Consult https://github.com/sveltejs/svelte-preprocess
  // for more information about preprocessors
  preprocess: preprocess()
};

export default config;
```

You can now specify that script blocks are written in TypeScript:

``` {data-language="typescript"}
<script lang="ts">
```

## Vite {#vite style="position:relative;"}

Vite supports importing `.ts` files out-of-the-box. It only performs
transpilation and not type checking. It also requires that some
`compilerOptions` have certain values. See the [Vite
docs](https://vitejs.dev/guide/features.html#typescript) for more
details.

## Webpack {#webpack style="position:relative;"}

### Install {#install-7 style="position:relative;"}

``` {data-language="shell"}
npm install ts-loader --save-dev
```

### Basic webpack.config.js when using Webpack 5 or 4 {#basic-webpackconfigjs-when-using-webpack-5-or-4 style="position:relative;"}

```js
const path = require('path');

module.exports = {
  entry: './src/index.ts',
  module: {
    rules: [
      {
        test: /\.tsx?$/,
        use: 'ts-loader',
        exclude: /node_modules/,
      },
    ],
  },
  resolve: {
    extensions: ['.tsx', '.ts', '.js'],
  },
  output: {
    filename: 'bundle.js',
    path: path.resolve(__dirname, 'dist'),
  },
};
```

See [more details on ts-loader
here](https://www.npmjs.com/package/ts-loader).

Alternatives:

-   [awesome-typescript-loader](https://www.npmjs.com/package/awesome-typescript-loader)

::: _attribution
© 2012-2023 Microsoft\
Licensed under the Apache License, Version 2.0.\
[https://www.typescriptlang.org/docs/handbook/integrating-with-build-tools.html](https://www.typescriptlang.org/docs/handbook/integrating-with-build-tools.html){._attribution-link}
:::
