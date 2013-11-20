# brunch-sha

[Brunch][1] plugin which generates a sha sum file as part of the `brunch build`
process.

[1]: http://brunch.io

## Usage

Install the plugin via npm with `npm install --save brunch-sha`.

Or, do manual install:

* Add `"brunch-sha": "x.y.z"` to `package.json` of your brunch app.
  Pick a plugin version that corresponds to your minor (y) brunch version.
* If you want to use git version of plugin, add
`"brunch-sha": "git+ssh://git@github.com:mutewinter/brunch-sha.git"`.

Specify [plugin settings](#settings) in config.coffee. For example:

```coffeescript
exports.config =
  # ...
  plugins:
    sha:
      shaFile: 'sha'
      ignore: /[\\/][.]/
```

## Settings

### appcache.ignore

A regular expression specifying paths to omit from the sha sum.

Default value : `/[/][.]/` (hidden files and files in hidden directories are ignored)

### appcache.shaFile

Output filename. For example:

```coffeescript
shaFile: "app.sha"
```

Default value : `"sha"`

## License

The MIT License (MIT)

Copyright (c) 2013 Jeremy Mack @mutewinter

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
