---
layout: post
title:  "Four tools every JavaScript team should use"
date:   2018-08-04 20:34:26
categories: javascript
comments: true
--- 

Whether you're starting a new JavaScript project, or hopping on an existing one, here are four tools your team should use.

# Yarn

[Yarn](https://yarnpkg.com/) will both be your build tool (to pass question 2 of the [Joel Test](https://www.joelonsoftware.com/2000/08/09/the-joel-test-12-steps-to-better-code/)) and your [package manager](https://en.wikipedia.org/wiki/Package_manager).

[Install yarn](https://yarnpkg.com/lang/en/docs/install) then enter this command to initialize your project:
```sh
yarn init
```

# ESLint

 Writing JavaScript without bugs is not easy. The first tool that will help you do that is [ESLint](https://eslint.org/).

Install ESLint:
```sh
yarn add -D eslint
```

Next, you need to configure ESLint, either by using the following command and answering a few questions:
```sh
yarn eslint --init
```
or by manually creating an ESLint configuration file at the root of your project named `.eslintrc.yml`.

It should at least contain the following line:
```yml
extends: 'eslint:recommended' 
```

Then, add the following lines to your package.json file:
```json
"scripts": {
    "lint": "eslint src --fix",
},
```

You now have at your disposal a command that prevents you from classic mistakes like [unused variables](https://eslint.org/docs/rules/no-unused-vars):
```sh
yarn lint
```

# Prettier

Team conventions about code formatting are great, but having to enforce them through code review comments is a pain. Fortunately, [Prettier](https://prettier.io/) is here to help. 

Install Prettier:
```sh
yarn add -D prettier
```

Since we are already using ESLint, we will run Prettier through ESLint using [eslint-plugin-prettier](https://github.com/prettier/eslint-plugin-prettier):
```sh
yarn add -D eslint-plugin-prettier
```

We will also follow [the plugin's author advice](https://github.com/prettier/eslint-plugin-prettier#recommended-configuration) and use [eslint-config-prettier](https://github.com/prettier/eslint-config-prettier) to disable all ESLint formatting rules, and leave this job to Prettier:
```sh
yarn add -D eslint-config-prettier
```

Edit your `.eslintrc.yml`: 
```yml
extends: 
  - eslint:recommended
  - plugin:prettier/recommended
```

And that's it, you no longer have to fight over spaces versus tabs, or single versus double quotes. The following command will now both warn you about errors and format your code:
```sh
yarn lint
```

# Flow

As I said earlier, writing JavaScript without bugs is not easy. When you add types to your JavaScript code, all of a sudden a lot of mistakes become obvious. That's why you should use [Flow](https://flow.org/).

First, install and initialize Flow:
```sh
yarn add -D flow-bin
yarn flow init
```

Then, annotate all your files with the following comment:
```js
// @flow
```

Finally, run the following command and enjoy type safety:
```sh
yarn flow
```

# Conclusion

Your safety harness is all set, you're ready to code! 

If you want to go further you can:
- add more eslint rules, using plugins like [eslint-plugin-import](https://www.npmjs.com/package/eslint-plugin-import)
- write [type annotations](https://flow.org/en/docs/types/), which will require you to use [babel](https://babeljs.io/)


If you need an example, you will find a showcase of all the tools I have presented in this article in [this repository](https://github.com/bastoche/javascript-tools).