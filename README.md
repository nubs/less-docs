# lesscss.org

> Official website and documentation for LESS/Less.js

## Quickstart

Assemble and Grunt are used to build the docs. To get started:

1. Download the docs
2. In the root of the project, run `npm install`
3. Run the `grunt` command to build the docs

If all worked properly, then you're ready to begin contributing to the docs!

### Documentation

All documentation content can be found in the `./content` directory. Please read the **contributing** section below if you wish to add documentation.


## The Plan

1. Clean up and organize all of the documentation in the [content](./content) directory, which means
2. Consistent naming conventions for files, consistent coding styles in documents
3. Organize information and favor individual files for sections of content, rather than long documents
4. Last, a new theme.


## Contributing
### Coding Style
> Please help us make the documentation as _consist, readable, and maintainable_ by conforming to these guidelines when contributing:

#### Markdown standards

* Use `#` for titles, not underlines. Underlines aren't as flexible, aren't always highlighted properly in code highlighters
* Always add a space between the `#` and the heading
* Wrap inline code with a **single backtick**,
* wrap blocks of code with **three backticks** (code fences).
* With code blocks, _always use the correct language_ after to the first code fence. Althought Ghtub does not highlight LESS, our documentation is more likely to show up in GitHub's and Google's search results when the correct language is used. Examples: pleas use `` ```less `` for LESS, and `` ```css `` for CSS.


#### LESS standards

* Two spaces for indentation, never tabs, and always use proper indentation
* Multiple-line formatting (one property and value per line)
* For multiple, comma-separated selectors, place each selector on it's own line
* Double quotes only, never single quotes
* Always a space after a property's colon (.e.g, `display: block;` and not `display:block;`)
* End _all_ lines with a semi-colon
* Attribute selectors, like `input[type="text"]` should always wrap the attribute's value in double quotes. This is important to do in your own code as well, for consistency and safety (see this [blog post on unquoted attribute values](http://mathiasbynens.be/notes/unquoted-attribute-values) that can lead to XSS attacks).
* When HTML is in your examples, use tags and elements appropriate for an HTML5 doctype (e.g., self-closing tags with _no trailing slash_)

Examples:

**Good**

```css
body {
  padding-top: 80px;
  font-size: 12px;
}
```

**Bad**

```css
body {
padding-top: 80px;
font-size: 12px;
}
```

**Bad**

```css
body { padding-top: 80px; font-size: 12px }
```

Also, please ensure that all documentation files should have globally unique names, regardless of where they are located in the repository. This makes it easier to use conveniences like file globbing, and it's good practice anyway.

### Feature Requests, Bugs and Pull Requests

* If you would like to request a feature, suggest an improvement, or report a bug, please [submit an Issue](https://github.com/cloudhead/less.js/issues?state=open).
* Feature requests are more likely to get attention if you include a clearly described use case.
* If you wish to submit a pull request, please [read this first](https://github.com/cloudhead/less.js/blob/master/CONTRIBUTING).md.

## Tools

The documentation site is generated using [Assemble](http://assemble.io). Please visit that project [to report bugs](https://github.com/assemble/assemble/issues?state=open), or to learn more about usage and customization.


## Build the docs

Update the project with the most recent metadata from the Less.js project, such as current version number, description, and so on, and then run Grunt with the following command:

```bash
node docs/pkg && grunt
```

## License
Copyright (c) 2013, Less.js Core Team, Contributors
Documentation source code released under the [MIT License](./LICENSE-MIT).