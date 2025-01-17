# JSDoc Generator - README

Automatic JSDoc generator for JavaScript, TypeScript and Typescript/JavaScript React.

---

## Features

Generates specific JSDoc for any supported TypeScript/JavaScript node.

It can be generated for a single node by explicitly calling the command `Generate JSDoc` or by using auto-completion:
![Generate JSDoc demo](demos/jsdoc-generator.generateJsdoc.gif)
Can also be generated for all supported TypeScript nodes in a single file that do not already have a JSDoc by calling the command `Generate JSDoc for the current file`:
![Generate JSDoc demo](demos/jsdoc-generator.generateJsdocFile.gif)

## Extension Settings

This extension contributes the following settings:

- `jsdoc-generator.descriptionPlaceholder`:  
  Set the description placeholder. Empty to disable.  
  Default: `"Description placeholder"`
- `jsdoc-generator.author`:  
  Set the value for the author tag.  
  Empty to disable, set to "author" to insert "author" as placeholder.  
  Default: `""`
- `jsdoc-generator.includeDate`:  
  When enabled, will include the date tag.  
  Default: `false`
- `jsdoc-generator.includeTime`:  
  When both this and jsdoc-generator.includeDate are enabled, will include the current local time in the date tag.  
  Default: `true`
- `jsdoc-generator.includeTypes`:  
  Whether to include types into the generated JSDoc.  
  Default: `true`
- `jsdoc-generator.includeParenthesisForMultipleTypes`:  
  When enabled, will include round brackets around union and intersection types.  
  Note that round brackets will still be used if manually put in the type or for union and intersection types which are also optional or mandatory.  
  Default: `true`
- `jsdoc-generator.descriptionForConstructors`:  
  "{Object}" will be replaced with the class name.  
  For default exported classes without a name `jsdoc-generator.descriptionPlaceholder` will be used instead.  
  Empty to disable.  
  Default: `"Creates an instance of {Object}."`
- `jsdoc-generator.functionVariablesAsFunctions`:  
  When enabled, will document variables with a function assigned as function declarations.  
  Disable to document like properties.  
  Default: `true`
- `jsdoc-generator.includeExport`:  
  When enabled, will include the export tag.  
  Disable to exclude it from the generated JSDoc.  
  Default: `true`
- `jsdoc-generator.includeAsync`:  
  When enabled, will include the async tag.  
  Disable to exclude it from the generated JSDoc.  
  Default: `true`
- `jsdoc-generator.customTags`:  
  When configured, will add custom tags by default.  
  Example:
  ```javascript
  "jsdoc-generator.customTags": [
    {
      "tag": "example",
      "placeholder": "Example placeholder"
    },
  ]
  ```

---

## Commands

- `Generate JSDoc`\
  Generates JSDoc for the TypeScript/JavaScript node the caret is in or on.
  Available also for auto-completion by typing `/**` at the start of a line.
- `Generate JSDoc for the current file`\
  Generates JSDoc for the currently open file for all TypeScript/JavaScript nodes that do not have one.\
  Eventually choosing a keyboard shortcut is left to the user.
- `Generate JSDoc for all TypeScript files`\
  Currently only prompts a message saying `This function is not available yet.`\
  Eventually choosing a keyboard shortcut is left to the user.

---

## Known Issues

Type inference does not work for variable declarations without an initializer.  
Some non [everyday types](https://www.typescriptlang.org/docs/handbook/2/everyday-types.html) are not correctly inferred and treated as any or empty object.

---

## Release Notes

### [1.3.0](https://github.com/Nyphet/jsdoc-generator/releases/tag/v1.3.0)

Added a new setting option to create custom tags.

### [1.2.0](https://github.com/Nyphet/jsdoc-generator/releases/tag/v1.2.0)

Added a new setting option to disable type inference and added support for JavaScript.

### [1.1.1](https://github.com/Nyphet/jsdoc-generator/releases/tag/v1.1.1)

Added two setting options.

### [1.1.0](https://github.com/Nyphet/jsdoc-generator/releases/tag/v1.1.0)

Added support for Typescript React.

### [1.0.0](https://github.com/Nyphet/jsdoc-generator/releases/tag/v1.0.0)

Initial release of JSDoc Generator.
