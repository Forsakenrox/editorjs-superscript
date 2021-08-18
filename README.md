![](https://badgen.net/badge/Editor.js/v2.0/blue)

# Superscript Tool

Superscript Tool for highlighting text-fragments for the [Editor.js](https://editorjs.io).


## Installation

### Install via NPM

Compile
```shell
npm i
npx webpack
```

### Download to your project's source dir

1. Upload folder `dist` from repository
2. Add `dist/bundle.js` file to your page.

Require this script on a page with Editor.js.

```html
<script src="..."></script>
```

## Usage

Add a new Tool to the `tools` property of the Editor.js initial config.

```javascript
var editor = EditorJS({
  ...
  
  tools: {
    ...
    superscript: {
      class: Superscript,
      shortcut: 'CMD+SHIFT+M',
    }
  },
  
  ...
});
```

## Config Params

This Tool has no config params

## Output data

Marked text will be wrapped with a `sup` tag with an `cdx-superscript` class.

```json
{
    "type" : "text",
    "data" : {
        "text" : "Create a directory for your module, enter it and run <sup class=\"cdx-superscript\">npm init</sup> command."
    }
}
```

