## Upload to Github Pages

```
npm i gh-pages
```

*In package.json*

```
"homepage": "https://sanjaypj.github.io/react-todo",
```

```
"scripts": {
    "deploy": "npm run build&&gh-pages -d build",
  },
```

Run `npm run deploy`
