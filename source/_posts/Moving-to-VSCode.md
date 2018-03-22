---
title: Moving to VSCode
date: 2018-03-22 12:20:41
subtitle:
tags:
---

I don't like change. I especially drag my feet when it comes to using a new tool for development. This is why I've been reluctant to change to VSCode from my comfy Atom IDE. Seeing the new [StackOverflow developer survey results](https://insights.stackoverflow.com/survey/2018/#technology-most-popular-development-environments) pushed me over to change finally. A majority of their users are now using Visual Studio Code. 

And I'm feeling the rewards from the switch pretty quickly. It wasn't as painful as I expected, but there are a few things that needed to be sorted out to put me back into my comfy workflow. I decided to document them below. 

# Extensions

### [Auto Close Tag](https://github.com/formulahendry/vscode-auto-close-tag) ⭐️⭐️

After typing in the closing bracket of the opening tag, the closing tag will be inserted automatically. Not totally sure if I'm going to keep this one. It doesn't always wrap the inner content very well in my jsx. Looking for a better recommendation. 

![](https://github.com/formulahendry/vscode-auto-close-tag/raw/master/images/usage.gif)

### [Auto Import](https://marketplace.visualstudio.com/items?itemName=steoates.autoimport) ⭐️⭐️⭐️⭐️

Automatically finds, parses and provides code actions and code completion for all available imports. 

![](https://gifyu.com/images/autoimport.gif)

### [Bookmarks](https://github.com/alefragnani/vscode-bookmarks) ⭐️

Mark lines in the editor and easily jump to them. I haven't used this yet, but I thought I might?

![](https://github.com/alefragnani/vscode-bookmarks/raw/master/images/bookmarks-toggle.png)

### [Bracket Pair Colorizer](https://github.com/CoenraadS/BracketPair) ⭐️


This extension allows matching brackets to be identified with colours. I actually ended up disabling this because I found it distracting, but some people really like it. 

![](https://github.com/CoenraadS/BracketPair/raw/master/images/example.png)

### [Code Spell Checker](https://github.com/Jason-Rev/vscode-spell-checker) ⭐️⭐️⭐️

A basic spell checker that works well with camelCase code. I actually found a spelling error in my copy on an application when I turned this on. 😬

### [Colorize](https://github.com/kamikillerto/vscode-colorize) ⭐️⭐️⭐️

Instantly visualize css colors in your css. It's a requirement nowadays.

![](https://raw.githubusercontent.com/kamikillerto/vscode-colorize/master/assets/demo.gif)

### [Easy Icons](https://github.com/jamesmaguire/vscode-easy-icons) ⭐️⭐️⭐️⭐️

I tried entirely too many icon themes. This one was my favorite. Icons per filetype is a *lot* more useful than I realized, especially in searching multiple files with similar names.

![](https://cloud.githubusercontent.com/assets/22332883/21157849/d152203c-c1df-11e6-8afe-8e48c07808a0.PNG)

### [Eslint](https://github.com/Microsoft/vscode-eslint) ⭐️⭐️⭐️⭐️

We use eslint, so this is a must-have. 

### [GitHub](https://github.com/KnisterPeter/vscode-github) ⭐️⭐️⭐️⭐️

Integration with GitHub. I really only use this to open the current file within GitHub within `cmd+shift+p` menu.

![](https://github.com/KnisterPeter/vscode-github/raw/master/images/create-pull-request.png)

### gitignore by michelemelluso ⭐️

Add file or folder to `.gitignore` by just right clicking on file.

### [Highlight Matching Tag](https://github.com/vincaslt/vscode-highlight-matching-tag) ⭐️⭐️⭐️⭐️

Highlight matching opening or closing tags

![](https://camo.githubusercontent.com/010b886fb93f49c56e4c7308ba0a5a1aca8a2db7/68747470733a2f2f692e696d67626f782e636f6d2f4455584c467657372e676966)

### [Import Cost](https://github.com/wix/import-cost) ⭐️⭐️⭐️⭐️⭐️

Display inline in the editor the size of the imported package. Having never had this before - I've fallen in love.

![](https://camo.githubusercontent.com/448786fbd2913985aca86fc648e4d2513f4d8354/68747470733a2f2f66696c652d776b62636e6c6376626e2e6e6f772e73682f696d706f72742d636f73742e676966)

### [JS Refactor](https://github.com/cmstead/js-refactor) ⭐️⭐️

Javascript automated refactoring tool. I haven't used this yet, but have great ambitions too. Especially for "Convert To Arrow Function".

### [Multiple cursor case preserve](https://github.com/Cardinal90/multi-cursor-case-preserve) ⭐️⭐️⭐️⭐️⭐️

Have you ever tried to change a single word in all variable names, but had your camelCase broken? This extension preserves selection case in these situations. I'm honestly surprised that so few people have this downloaded. I was super excited to find this.

![](https://github.com/Cardinal90/multi-cursor-case-preserve/raw/master/images/Example.gif)

### [Npm Intellisense](https://github.com/ChristianKohler/NpmIntellisense) ⭐️⭐️⭐️⭐️

Autocompletes npm modules in import statements.

![](https://github.com/ChristianKohler/NpmIntellisense/raw/master/images/auto_complete.gif)

### [One Dark Pro](https://github.com/Binaryify/OneDark-Pro) ⭐️⭐️⭐️⭐️

My favorite theme! 

![](https://raw.githubusercontent.com/Binaryify/OneDark-Pro/master/static/js.png)

### [Log Output Colorizer](https://github.com/IBM-Cloud/vscode-log-output-colorizer) ⭐️⭐️⭐️

Adds syntax colorization for `*.log` files. People love to send me `.log` files. 😐

![](https://raw.githubusercontent.com/IBM-Bluemix/vscode-log-output-colorizer/master/github-assets/screenshot-4.jpg)

### [Path Autocomplete](https://github.com/ionutvmi/path-autocomplete) ⭐️⭐️⭐️

Provides path completion.

![](https://raw.githubusercontent.com/ionutvmi/path-autocomplete/master/demo/path-autocomplete.gif)

### [Search node_modules](https://github.com/jasonnutter/vscode-search-node-modules) ⭐️⭐️⭐️⭐️

Since `node_modules` are excluded from my global search, I need a way to dig into them when they have bugs. This is an ok way to do that. I wish I could search for specific code within the node_module more easily though.

![](https://raw.githubusercontent.com/jasonnutter/vscode-search-node-modules/master/img/demo.gif)

### [SVG Viewer](https://github.com/cssho/vscode-svgviewer) ⭐️⭐️

You can actually view SVG files in your editor.

![](https://github.com/cssho/vscode-svgviewer/raw/master/img/from_context.gif)

### [Swig](https://marketplace.visualstudio.com/items?itemName=zhutian.swig) ⭐️

Swig support. Yes, we have some swig templates. We need to move off of them. 

### [TODO Highlight](https://github.com/wayou/vscode-todo-highlight) ⭐️⭐️⭐️

Highlights `TODO` and `FIXME` in code. I didn't realize how many `TODO`s were in my code until I installed this. 😅

![](https://github.com/wayou/vscode-todo-highlight/raw/master/assets/material-night-eighties.png)

### [Version Lens](https://github.com/vscode-contrib/vscode-versionlens) ⭐️⭐️⭐️⭐️⭐️

Shows package version information for npm and bower. Amazing. What I've always wanted.

![](https://github.com/vscode-contrib/vscode-versionlens/raw/master/images/animated-preview.gif)

### [Random Data Generator](https://github.com/jrebocho/vscode-random) ⭐️⭐️

Generates random data directly into VS Code. I was hoping this would be useful in my fixtures.

![](https://raw.githubusercontent.com/jrebocho/vscode-random/master/images/vscode-random-screen.gif)


# Keybindings

The quickopen is something really weird and I wasn't having it. Remapped this to `cmd+t`

```
{ "key": "cmd+t", "command": "workbench.action.quickOpen" }
```

Also, I needed to map my 'go to current file in explorer' key. 

```
{ "key": "shift+cmd+\\", "command": "editor.action.jumpToBracket" }
```

`cmd+shift+e` - shows editor in left hand side. Just memorize this.
`cmd+shift+e` - shows extensions in left hand side.

# vscode settings.json

This is my `settings.json` within the `vscode` folder. This ensures that eslint auto fixes on save, *but* lets me put a `debugger` in my code!

```json
{
  "git.ignoreLimitWarning": true,
  "eslint.enable": true,
  "eslint.alwaysShowStatus": true,
  "eslint.autoFixOnSave": true,
  "eslint.options": {
    "rules": {
      "no-debugger": "off"
    }
  }
}
```

# Settings

These are my settings. Some of these are extension specific. Notice this will turn on [Intellisense for `cypress.json` files](https://on.cypress.io/configuration#IntelliSense).

```json
{
    "editor.fontFamily": "Fira Code, Monaco, 'Courier New', monospace",
    "editor.fontSize": 14,
    "editor.lineHeight": 24,
    "editor.fontLigatures": true,
    "editor.tabSize": 2,
    "editor.minimap.enabled": false,
    "editor.formatOnPaste": true,
    "editor.wordWrap": false,
    "explorer.openEditors.visible": 0,
    "editor.multiCursorModifier": "ctrlCmd",
    "editor.snippetSuggestions": "top",
    "editor.renderWhitespace": "none",
    "editor.renderControlCharacters": true,
    "workbench.colorTheme": "One Dark Pro",
    "bold_folder_labels": true,
    "font_options": [
        "gray_antialias",
        "subpixel_antialias"
    ], 
    "indent_guide_options": [
        "draw_normal",
        "draw_active"
    ],
    "overlay_scroll_bars": "enabled",
    "workbench.activityBar.visible": false,
    "workbench.startupEditor": "newUntitledFile",
    "eslint.enable": false,
    "sublimeTextKeymap.promptV3Features": true,
    "json.schemas": [
        {
            "fileMatch": [
                "cypress.json"
            ],
            "url": "https://on.cypress.io/cypress.schema.json"
        },
        {
            "fileMatch": [
                "/bower.json"
            ],
            "url": "http://json.schemastore.org/bower"
        }
    ],
    "workbench.statusBar.visible": true,
    "workbench.iconTheme": "easy-icons",
    "files.associations": {
        "*.jsx": "javascriptreact"
    }
}
```

# Intellisense for Cypress

Add `/// <reference types="Cypress" />` to top of `.js` or `.ts` test files.

![](https://docs.cypress.io/img/guides/typescript-intellisense-with-reference.d0d2b2de.gif)

# Gotchas

## jsconfig.json

I have to add this inside the source folder of any project where I am used mobx, just to avoid the warning for Experimental Decorators. Not happy about it, but whatever.

```json
{
  "compilerOptions": {
      "experimentalDecorators": true
  }
}
```

## Search

Search was weird at first and took getting used to. But now I love it more than atom. 

![](https://user-images.githubusercontent.com/1271364/37787077-902e86d8-2dd4-11e8-9d90-6657abaccd1b.png)

