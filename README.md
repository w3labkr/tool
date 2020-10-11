# tool-init

Configuration settings that are used frequently.

## Theme

```
{
  "workbench.colorTheme": "One Dark Pro",
  "workbench.iconTheme": "vscode-icons",
}
```

**Reference**
<https://marketplace.visualstudio.com/items?itemName=zhuangtongfa.Material-theme>   
<https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons>   

---

## Files

```
{
  "files.associations": {
    "*.html": "html",
    "*.json": "json",
    "**/.*rc": "json"
  },
  "files.exclude": {
    "**/.git": true,
    "**/.svn": true,
    "**/.hg": true,
    "**/.DS_Store": true,
    "**/.history": true
  },
  "files.watcherExclude": {
    "**/.history": true
  },
}
```

---

## Search

```
{
  "search.exclude": {
    "**/node_modules": true,
    "**/bower_components": true,
    "**/.history": true
  },
}
```

## Editor

```
{
  "editor.suggestSelection": "first",
  "editor.formatOnSave": false,
  "editor.tabSize": 2,
  "editor.wordWrap": "on",
  "editor.detectIndentation": false,
  "editor.codeActionsOnSave": {
    "source.fixAll.stylelint": true,
    "source.fixAll.eslint": true
  },
}
```

---

## Autoprefixer

**VSCode**   
Edit the configuration file settings.json.
```
{
  "autoprefixer.options": {
    "overrideBrowserslist": [
      "> 0%"
    ]
  },
}
```

**Reference**
<https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-autoprefixer>   

---

## Prettier

**Terminal**
```
$ npm i -g prettier
```

**VSCode**   
Edit the configuration file settings.json.

```
{
  "prettier.trailingComma": "es5",
  "prettier.useTabs": false,
  "prettier.tabWidth": 2,
  "prettier.semi": true,
  "prettier.singleQuote": false,
  "prettier.printWidth": 80,
  "[html]": {
    "editor.formatOnSave": false,
    "editor.codeActionsOnSave": {
      "source.fixAll.stylelint": true
    }
  },
  "[css]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[scss]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascript]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascriptreact]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[typescript]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[typescriptreact]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[json]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[jsonc]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[graphql]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
}
```

**Reference**
<https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode>   

---

## Stylelint

**Terminal**
```
$ npm i -g stylelint stylelint-scss stylelint-order stylelint-config-standard stylelint-config-prettier 
```

**VSCode**   
Edit the configuration file settings.json.
```
{
  "editor.formatOnSave": false,
  "editor.codeActionsOnSave": {
    "source.fixAll.stylelint": true,
  },
  "css.validate": false,
  "less.validate": false,
  "scss.validate": false,
  "stylelint.enable": true,
  "stylelint.config": {
    "plugins": ["stylelint-scss", "stylelint-order"],
    "extends": ["stylelint-config-standard", "stylelint-config-prettier"],
    "rules": {
      "indentation": 2,
      "declaration-block-trailing-semicolon": "always",
      "selector-pseudo-element-colon-notation": "single",
      "font-family-no-missing-generic-family-keyword": null,
      "comment-empty-line-before": [
        "always",
        {
          "except": ["first-nested"],
          "ignore": ["after-comment"]
        }
      ],
      "rule-empty-line-before": ["never"],
      "order/order": [],
      "order/properties-order": []
    }
  },
  "[html]": {
    "editor.codeActionsOnSave": {
      "source.fixAll.stylelint": true
    }
  },
  "[css]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[scss]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
}
```

**Reference**
<https://stylelint.io/>   
<https://github.com/stylelint/stylelint-config-standard>   
<https://maximgatilin.github.io/stylelint-config/>   
<https://marketplace.visualstudio.com/items?itemName=stylelint.vscode-stylelint>   

---

## ESLint

**Terminal**
```
$ npm i -g eslint eslint-plugin-prettier eslint-config-prettier
```

**Global**
```
$ npm bin -g
$ vi /Users/[user]/.bash_profile

...
# The next line makes the node bin command global.
PATH=$PATH:~/node/bin
```

**Permission**
```
$ sudo su
$ chown [user]:group /usr/local/lib/node_modules
$ chown -R [user]:group /Users/[user]/node/lib
$ chown -R [user]:group /Users/[user]/node/bin
```

**Configure**
```
$ npm init -y
$ eslint --init
```

**VSCode**   
Edit the configuration file settings.json.
```
{
  "editor.formatOnSave": false,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact"
  ],
  "[javascript]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[json]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[jsonc]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[graphql]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
}
```

**Reference**   
<https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint>   

---

## PHP Intelephense

**VSCode**   
Edit the configuration file settings.json.

```
{
  "intelephense.diagnostics.undefinedTypes": false,
  "intelephense.diagnostics.undefinedFunctions": false,
  "intelephense.diagnostics.undefinedConstants": false,
  "intelephense.diagnostics.undefinedClassConstants": false,
  "intelephense.diagnostics.undefinedMethods": false,
  "intelephense.diagnostics.undefinedProperties": false,
  "intelephense.diagnostics.undefinedVariables": false,
  "intelephense.files.exclude": [
    "**/.git/**",
    "**/.svn/**",
    "**/.hg/**",
    "**/CVS/**",
    "**/.DS_Store/**",
    "**/.vscode/**",
    "**/.history/**",
    "**/node_modules/**",
    "**/bower_components/**",
    "**/vendors/**",
    "**/vendor/**",
    "**/build/**",
    "**/packages/**",
    "**/wp-includes/**",
    "**/wp-admin/**"
  ],
}
```

**Reference**   
<https://marketplace.visualstudio.com/items?itemName=bmewburn.vscode-intelephense-client>   

---

## phpfmt - PHP formatter

**VSCode**   
Edit the configuration file settings.json.

```
{
  "phpfmt.passes": [
    "PSR2KeywordsLowerCase",
    "PSR2LnAfterNamespace",
    "PSR2CurlyOpenNextLine",
    "PSR2ModifierVisibilityStaticOrder",
    "PSR2SingleEmptyLineAndStripClosingTag",
    "ReindentSwitchBlocks"
  ],
  "phpfmt.exclude": ["ReindentComments", "StripNewlineWithinClassBody"],
  "phpfmt.psr2": false,
  "phpfmt.indent_with_space": 2,
  "[php]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "kokororin.vscode-phpfmt"
  },
}
```

**Reference**   
<https://marketplace.visualstudio.com/items?itemName=kokororin.vscode-phpfmt>   
