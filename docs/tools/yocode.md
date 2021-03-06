---
Order: 2
Area: tools
TOCTitle: Extension Generator
ContentId: C733425A-3F06-4DB9-90A0-472EF1DB58D3
PageTitle: The Yo Code Visual Studio Code Extension Generator
DateApproved: 6/6/2016
MetaDescription: Easily create VS Code extensions and customizations with the Yo Code generator.
---
# Yo Code - Extension Generator

We have written a [Yeoman generator](https://github.com/Microsoft/vscode-generator-code) to help get you started.

## Install the Generator

Install Yeoman and the VS Code Extension generator from the command prompt:

```bash
npm install -g yo generator-code
```

## Run Yo Code

The Yeoman generator will walk you through the steps required to create your customization or extension prompting for the required information.

To launch the generator simply type the following in a command prompt:

```bash
yo code
```

![yo code output](images/yocode/yocode.png)

## Generator Options

The generator can either create an extension skeleton for a new extension or create a ready-to-use extension for languages, themes or snippets based on existing TextMate definition files.

### New Extension in TypeScript

Creates an extension skeleton implementing a 'hello world' command. Use this as a starting point for your own extension.

* Prompts for the extension identifier and will create a folder of that name in the current directory
* Creates a base folder structure with a source, test and output folder
* Templates out a `package.json` file and an extension main file
* Sets-up `launch.json` and `tasks.json` so that F5 will compile and run your extension and attach the debugger
* Optionally sets up a Git repository

Once created, open VS Code on the created folder. The folder contains a file `vsc-extension-quickstart.md` as a quick guide with the next steps. The extension is setup so that you get IntelliSense for the extension API.

### New Extension in JavaScript

Does the same as `New Extension (TypeScript)`, but for JavaScript. The extension is setup so that you get IntelliSense for the extension API.

### New Color Theme

Creates an extension that contributes a new color theme based on an existing TextMate color theme.

* Prompts for the location (URL or file path) of the existing TextMate color theme (.tmTheme). This file will be imported into the new extension.
* Prompts for the color theme name as well as the color base theme (light or dark)
* Prompts for the extension identifier and will create a folder of that name in the current directory

Once created, open VS Code on the created folder and run the extension to test the new theme.
Check out `vsc-extension-quickstart.md`. It's a quick guide with the next steps.

### New Language Support

Creates an extension that contributes a language with colorizer.

* Prompts for the location (URL or file path) of an existing TextMate language file (.tmLanguage, .plist or .json). This file will be imported to the new extension
* Prompts for the extension identifier and will create a folder of that name in the current directory

Once created, open VS Code on the created folder and run the extension to test the colorization. Check out `vsc-extension-quickstart.md` for the next steps. Have a look at the language configuration file that has been created and defines configuration options such what style of comments and brackets the language uses.

### New Code Snippets

Creates an extension that contributes new code snippets.

* Prompts for the folder location that contains TextMate snippets (.tmSnippet) or Sublime snippets (.sublime-snippet). These file are converted to a VS Code snippet file.
* Prompts for the language for which these snippets will be active
* Prompts for the extension identifier and will create a folder of that name in the current directory

Once created, open VS Code on the created folder and run the extension to test the snippets. Check out `vsc-extension-quickstart.md` for the next steps.

## Loading an Extension

To load an extension, you need to copy the files to your VS Code extensions folder. We cover this in detail here: [Installing Extensions](/docs/extensions/install-extension.md#your-extensions-folder).

## Next Steps

* [Publishing Tool](/docs/tools/vscecli.md) - Learn how to publish your extensions to the VS Code Marketplace
* [Hello World](/docs/extensions/example-hello-world.md) - Try the 'Hello World' walkthrough to build your first extension 

## Common Questions

**Q: The `yo code` generator doesn't respond to arrow keys on Windows 10.**

**A:** Try starting the Yeoman generator with just `yo` and then select the `Code` generator.

![yo workaround](images/yocode/yo-workaround.png)
