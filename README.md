# grunt-combine-mq
[![NPM version][npm-image]][npm-url]

> Combine matching media queries into one media query definition. Useful for CSS generated by preprocessors using nested media queries.

## Getting Started
This plugin requires Grunt `~0.4.5`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```sh
npm install grunt-combine-mq --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-combine-mq');
```

## The 'combine_mq' task

### Overview
In your project's Gruntfile, add a section named `combine_mq` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  combine_mq: {
    options: {
      // Task-specific options go here.
    },
    your_target: {
      // Target-specific file lists and/or options go here.
    }
  }
});
```

### Usage Examples

#### Default Options
In this example, the default options are used to do combine media queries in all `.css` files in the `src` directory and outputs them to the `dist` directory.

```js
grunt.initConfig({
  combine_mq: {
    default_options: {
      expand: true,
      cwd: 'src',
      src: '*.css',
      dest: 'dist/'
    }
  }
});
```

#### New filename
In this example, the custom options are used to do combine media queries in the `test.css` files in the `src` directory and outputs to the `dist` directory with a new filename - `new_filename.css`.

```js
grunt.initConfig({
  combine_mq: {
    new_filename: {
    	options: {
				beautify: false
    	},
      src: 'src/test.css',
      dest: 'dist/new_filename.css'
    }
  }
});

```

## Contributing
[![Build Status][travis-image]][travis-url]

To contribute check the [GitHub issues](https://github.com/buildingblocks/grunt-combine-mq/issues) then work away!

In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

* Install [editorconfig-sublime](https://github.com/sindresorhus/editorconfig-sublime) for Sublime Text to help with consistent code formatting.
* Commit messages loosely adhere to [these guidelines](https://github.com/angular/angular.js/blob/master/CONTRIBUTING.md#commit).
* Versioning adheres to [Semver](http://semver.org).

## Release History
* 11-04-15 - v0.9.0 - Logs out original and processed file sizes
* 07-04-15 - v0.8.0 - Updates to [Node combine-mq v0.8.0](https://github.com/frontendfriends/node-combine-mq/releases/tag/v0.8.0). See [releases](https://github.com/frontendfriends/node-combine-mq/releases) for more info.
* 22-12-14 - v0.7.0 - Updates to latest node package, adds tasks and rewrites tests for it
* 21-12-14 - v0.6.0 - Updates to [Node combine-mq v0.6.0](https://github.com/frontendfriends/node-combine-mq/releases/tag/v0.6.0). See [releases](https://github.com/frontendfriends/node-combine-mq/releases) for more info.
* 21-12-14 - v0.5.0 - Updates to [Node combine-mq v0.5.0](https://github.com/frontendfriends/node-combine-mq/releases/tag/v0.5.0). See [releases](https://github.com/frontendfriends/node-combine-mq/releases) for more info.
* 27-09-14 - v0.2.0 - Adds tests.
* 26-09-14 - v0.1.0 - Initial release.

See [releases](https://github.com/frontendfriends/grunt-combine-mq/releases) for more info.

## License
[MIT License](http://building-blocks.mit-license.org)

[npm-image]: https://badge.fury.io/js/grunt-combine-mq.svg
[npm-url]: https://npmjs.org/package/grunt-combine-mq
[travis-image]: https://travis-ci.org/frontendfriends/grunt-combine-mq.svg
[travis-url]: https://travis-ci.org/frontendfriends/grunt-combine-mq
