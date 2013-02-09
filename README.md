# grunt-append-templates

> Append all templates views in index.html body in script tags.

## Getting Started
_If you haven't used [grunt][] before, be sure to check out the [Getting Started][] guide._

From the same directory as your project's [Gruntfile][Getting Started] and [package.json][], install this plugin with the following command:

```bash
npm install grunt-append-templates --save-dev
```

Once that's done, add this line to your project's Gruntfile:

```js
grunt.loadNpmTasks('grunt-append-templates');
```

If the plugin has been installed correctly, running `grunt --help` at the command line should list the newly-installed plugin's task or tasks. In addition, the plugin should be listed in package.json as a `devDependency`, which ensures that it will be installed whenever the `npm install` command is run.

[grunt]: http://gruntjs.com/
[Getting Started]: https://github.com/gruntjs/grunt/blob/devel/docs/getting_started.md
[package.json]: https://npmjs.org/doc/json.html

## The "append_templates" task

### Overview
In your project's Gruntfile, add a section named `append_templates` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  append_templates: {
    options: {
      tag: 'script',
      type: 'text/x-template',
      layout: 'app/templates/layout.html'
    },
    your_target: {
      files: {
				‘path/to/index.html’: [path/to/templates/*.html]
			}
    },
  },
})
```

### Options

#### options.tag
Type: `String`
Default value: `script`

A string value that is used to do include each template as html content.

#### options.type
Type: `String`
Default value: `text/x-template`

A string value that is used to do represent to template you used in your project.

#### options.layout
Type: `String`
Default value: `app/templates/layout.html`

The value represent the default layout file of your project.

### Usage Examples

#### Default Options
In this example, the default options are used to insert all templates of the project in the default layout file.

```js
grunt.initConfig({
  append_templates: {
    options: {},
    files: {
      ‘public/index.html’: [‘app/templates/**/*.html’],
    },
  },
})
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [grunt][].

## Release History
0.1.0 - Initial Version
