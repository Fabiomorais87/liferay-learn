# Understanding Bundler Configuration Presets

The liferay-npm-bundler comes with a default configuration preset: [`liferay-npm-bundler-preset-standard`](https://github.com/liferay/liferay-npm-build-tools/tree/master/packages/liferay-npm-bundler-preset-standard). You may omit the `liferay-npm-bundler` prefix from the npm package name in your `.npmbundlerrc` file. This preset configures several plugins for the build process and is automatically used (even if the `.npmbundlerrc` is missing), unless you override it with one of your own. Running the liferay-npm-bundler with this preset applies the [config file](https://github.com/liferay/liferay-npm-build-tools/blob/master/packages/liferay-npm-bundler-preset-standard/config.json) from `liferay-npm-bundler-preset-standard`:

```json
{
  "/": {
    "plugins": ["resolve-linked-dependencies"],
    ".babelrc": {
      "presets": ["liferay-standard"]
    },
    "post-plugins": ["namespace-packages", "inject-imports-dependencies"]
  },
  "*": {
    "copy-plugins": ["exclude-imports"],
    "plugins": ["replace-browser-modules"],
    ".babelrc": {
      "presets": ["liferay-standard"]
    },
    "post-plugins": [
      "namespace-packages",
      "inject-imports-dependencies",
      "inject-peer-dependencies"
    ]
  }
}
```

The configuration above states that for all npm packages (`*`) the pre-process phase (`plugins`) must run the `replace-browser-modules` plugin. Setting this to `post-plugins` runs it during the post phase instead. 

```{note}
You can override configuration preset values by adding your own configuration to your project's `.npmbundlerrc` file. For instance, using the configuration preset example above, you can define your own `.babelrc` value in `.npmbundlerrc` file to override the defined "liferay-standard" babelrc preset.
```

## Liferay Standard Preset

The [`liferay-standard` preset](https://github.com/liferay/liferay-npm-build-tools/tree/master/packages/babel-preset-liferay-standard) applies the following plugins to packages:

* [exclude-imports](https://github.com/liferay/liferay-npm-build-tools/tree/master/packages/liferay-npm-bundler-plugin-exclude-imports): Exclude packages declared in the `imports` section from the build.

* [inject-imports-dependencies](https://github.com/liferay/liferay-npm-build-tools/tree/master/packages/liferay-npm-bundler-plugin-inject-imports-dependencies): Inject dependencies declared in the `imports` section in the dependencies' `package.json` files.

* [inject-peer-dependencies](https://github.com/liferay/liferay-npm-build-tools/tree/master/packages/liferay-npm-bundler-plugin-inject-peer-dependencies): Inject declared peer dependencies (as they are resolved in the project's `node_modules` folder) in the dependencies' `package.json` files.

* [namespace-packages](https://github.com/liferay/liferay-npm-build-tools/tree/master/packages/liferay-npm-bundler-plugin-namespace-packages): Namespace package names based on the root project's package name to isolate packages per project and avoid collisions. This prepends `<project-package-name>$` to each package name appearance in `package.json` files.

* [replace-browser-modules](https://github.com/liferay/liferay-npm-build-tools/tree/master/packages/liferay-npm-bundler-plugin-replace-browser-modules): Replaces the server side files for modules listed under `browser`/`unpkg`/`jsdelivr` section of `package.json` with their browser counterparts. 

* [resolve-linked-dependencies](https://github.com/liferay/liferay-npm-build-tools/tree/master/packages/liferay-npm-bundler-plugin-resolve-linked-dependencies): Replace linked dependencies versions appearing in `package.json` files (those obtained from local file system or GitHub, for example) by their real version numbers, as resolved in the project's `node_modules` directory.

## Liferay Babel Preset

The bundler also runs Babel with the [babel-preset-liferay-standard](https://github.com/liferay/liferay-npm-build-tools/tree/master/packages/babel-preset-liferay-standard) preset, which invokes the following plugins:

* [babel-plugin-normalize-requires](https://github.com/liferay/liferay-npm-build-tools/tree/master/packages/babel-plugin-normalize-requires): Normalize AMD `require()` calls.

* [babel-plugin-transform-node-env-inline](https://github.com/babel/minify/tree/master/packages/babel-plugin-transform-node-env-inline): Inline the `NODE_ENV` environment variable, and if it's part of a binary expression (eg. `process.env.NODE_ENV === "development"`), then statically evaluate and replace it.

* [babel-plugin-minify-dead-code-elimination](https://www.npmjs.com/package/babel-plugin-minify-dead-code-elimination): Inline bindings when possible. Tries to evaluate expressions and prunes unreachable as a result.

* [babel-plugin-wrap-modules-amd](https://github.com/liferay/liferay-npm-build-tools/tree/master/packages/babel-plugin-wrap-modules-amd): Wrap modules inside an AMD `define()` module.

* [babel-plugin-name-amd-modules](https://github.com/liferay/liferay-npm-build-tools/tree/master/packages/babel-plugin-name-amd-modules): Name AMD modules based on package name, version, and module path.

* [babel-plugin-namespace-modules](https://github.com/liferay/liferay-npm-build-tools/tree/master/packages/babel-plugin-namespace-modules): Namespace modules based on the root project's package name, prepending `<project-package-name>$`. Wrap modules inside an AMD `define()` module for each module name appearance (in `define()` or `require()` calls) so that the packages are localized per project and don't clash.

* [babel-plugin-namespace-amd-define](https://github.com/liferay/liferay-npm-build-tools/tree/master/packages/babel-plugin-namespace-amd-define): Add a prefix to AMD `define()` calls (by default `Liferay.Loader.`).

Now you know the available configuration presets for `.npmbundlerrc` and how they work.
