# Shopify Development Config
This simple package.json contains all the necessary Shopify plugins and rules for developing Shopify themes.

<p align="center">
  <img src="https://imgur.com/w1i9FBI.jpg" width="600" alt="Shopify Image"/>
</p>


Package.json contains:
* @shopify/prettier-config
* @shopify/babel-preset 
* @shopify/eslint-plugin 
* @shopify/stylelint-plugin.

#### Note: If you already have a package.json, then you may wish to simply copy some of the dependencies and rules like so:
Dev Dependencies - Usually placed below "Dependencies"
```npm
  "devDependencies": {
    "@shopify/babel-preset": "23.1.2",
    "@shopify/eslint-plugin": "^39.0.2",
    "@shopify/prettier-config": "^1.1.2",
    "@shopify/stylelint-plugin": "^10.0.1",
    "babel-core": "6.26.3",
    "eslint": "^7.12.1",
    "prettier": "^2.1.2",
    "stylelint": "^13.7.2"
  },
```



Rules and configurations - Place below any other configurations you already have.
```npm
  "babel": {
    "presets": [
      "@shopify/babel-preset/web"
    ]
  },
  "eslintConfig": {
    "extends": [
      "plugin:shopify/esnext",
      "plugin:shopify/prettier",
      "plugin:shopify/stylelint"
    ]
  },
  "prettier": "@shopify/prettier-config",
  "stylelint": {
    "extends": [
      "@shopify/stylelint-plugin",
      "@shopify/stylelint-plugin/prettier"
    ]
  }
```

##### Install packages
```shell script
yarn install
```

