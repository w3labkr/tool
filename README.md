# tool-init

Configuration settings that are used frequently.

## Autoprefixer

**VSCode**   
Edit the configuration file settings.json.
```
{
  "autoprefixer.options": {
    "overrideBrowserslist": [
      "last 2 version",
      "> 0.1%",
      "IE > 8"
    ]
  },
}
```

---

## ESLint

**VSCode**   
Edit the configuration file settings.json.
```
{
  "editor.formatOnSave": false,
  "editor.codeActionsOnSave": {
  "source.fixAll.eslint": true
  },
}
```

---

## TSLint

**VSCode**   

Edit the configuration file settings.json.
```
{
  "editor.formatOnSave": false,
  "editor.codeActionsOnSave": {
  "source.fixAll.tslint": true
  },
}
```

---

## Prettier

**VSCode**   
Edit the configuration file settings.json.
```
{
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true,
    "source.fixAll.tslint": true
  },
  "[javascript]": {
    "editor.formatOnSave": true
  },
  "[javascriptreact]": {
    "editor.formatOnSave": true
  },
  "[typescript]": {
    "editor.formatOnSave": true
  },
  "[typescriptreact]": {
    "editor.formatOnSave": true
  },
  "[json]": {
    "editor.formatOnSave": true
  },
  "[graphql]": {
    "editor.formatOnSave": true
  },
  "files.autoSave": "afterDelay",
  "prettier.trailingComma": "all",
  "prettier.tabWidth": 2,
  "prettier.semi": true,
  "prettier.singleQuote": true
}
```
