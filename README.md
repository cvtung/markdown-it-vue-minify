# markdown-it-vue-minify
[![Build Status](https://www.travis-ci.com/cvtung/markdown-it-vue-minify.svg?branch=master)](https://www.travis-ci.com/cvtung/markdown-it-vue-minify)

> The basic Vue lib for markdown-it (No chart and FontAwesome)

## Install

```sh
npm install markdown-it-vue-minify
```

## Supports

- Image size and Viewer
- Official markdown syntax.
- GFM TOC
- GFM style
- emoji
- Subscript/Superscript
- [AsciiMath](http://asciimath.org/)
- info | error | warning message tip

## Plugin list

- markdown-it
- markdown-it-emoji
- markdown-it-sub
- markdown-it-sup
- markdown-it-footnote
- markdown-it-deflist
- markdown-it-abbr
- markdown-it-ins
- markdown-it-mark
- markdown-it-katex
- markdown-it-task-lists
- markdown-it-highlight
- markdown-it-latex
- markdown-it-container
- markdown-it-github-toc
- markdown-it-source-map
- markdown-it-link-attributes

internal plugin list:

- markdown-it-image
- markdown-it-link-attributes
- markdown-it-highlight

## Options

use `options` property to sepcial the options of markdow-it and markdown-it-plugins.

```html
<markdown-it-vue class="md-body" :content="content" :options="options" />
```

```js
options: {
  markdownIt: {
    linkify: true
  },
  linkAttributes: {
    attrs: {
      target: '_blank',
      rel: 'noopener'
    }
  }
}
```

more markdown-it options see <https://markdown-it.github.io/markdown-it/>.

amd default plugins options:

```js
{
  linkAttributes: {
    attrs: {
      target: '_blank',
      rel: 'noopener'
    }
  },
  katex: {
    throwOnError: false,
    errorColor: '#cc0000'
  },
  githubToc: {
    tocFirstLevel: 2,
    tocLastLevel: 3,
    tocClassName: 'toc',
    anchorLinkSymbol: '',
    anchorLinkSpace: false,
    anchorClassName: 'anchor',
    anchorLinkSymbolClassName: 'octicon octicon-link'
  },
  image: {
    hAlign: 'left',
    viewer: true
  }
}
```

## More plugins

it can add your plugin to markdown-it-vue by the `use` method.

```js
this.$refs.myMarkdownItVue.use(MyMarkdownItPlugin)
```

## support hilight lang

PR for you lang wich you want.

- html
- json
- css
- shell
- bash
- C
- Java
- Python
- C++
- C#
- PHP
- SQL
- R
- Swift
- Go
- MATLAB
- Ruby
- Perl
- Objective-C
- Rust
- Dart
- Delphi
- D
- Kotlin
- Scala
- SAS
- Lisp
- Lua
- Ada
- Fortran
- PowerShell
- VBScript
- VBscript-html
- Groovy
- Julia
- Julia-repl
- LabVIEW
- Haskell
- ActionScript
- Scheme
- TypeScript
- F#
- Prolog
- Erlang

## image size

```md
![Minion](https://octodex.github.com/images/minion.png =x100)
![Stormtroopocat](https://octodex.github.com/images/stormtroopocat.jpg "The Stormtroopocat" =100x100)
```

## Usage

```vue
<template>
  <div>
    <markdown-it-vue class="md-body" :content="content" />
  </div>
</template>

<script>
import MarkdownItVue from 'markdown-it-vue'
import 'markdown-it-vue/dist/markdown-it-vue.css'
export default {
  components: {
    MarkdownItVue
  },
  data() {
    return {
      content: '# your markdown content'
    }
  }
}
</script>
```

## ScreenShot

![markdown-it-vue-minify](https://github.com/cvtung/markdown-it-vue-minify/blob/master/doc/markdown-it-vue-minify.png?raw=true)

## License

[MIT](https://github.com/cvtung/markdown-it-vue-minify/blob/master/LICENSE)
