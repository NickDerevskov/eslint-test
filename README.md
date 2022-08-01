# Project to show an issue with eslint.

When you want to use React + Typescript + Airbnb guide. Eslint will install an Airbnb guide to js, not ts.

How to reproduce:

1. npm init
2. npx eslint —init
3. eslint —init will install eslint
4. How would you like to use ESLint? To check syntax, find problems, and enforce code style
5. What type of modules does your project use? JavaScript modules (import/export) (doesn't matter)
6. Which framework does your project use? React
7. Does your project use TypeScript? Yes
8. Where does your code run? Browser (doesn't matter)
9. How would you like to define a style for your project? Use a popular style guide
10. Which style guide do you want to follow? airbnb
11. What format do you want your config file to be in? json (doesn't matter)
12. Install: eslint-plugin-react@^7.28.0 @typescript-eslint/eslint-plugin@latest eslint-config-airbnb@latest eslint@^7.32.0 || ^8.2.0 eslint-plugin-import@^2.25.3 eslint-plugin-jsx-a11y@^6.5.1 eslint-plugin-react-hooks@^4.3.0 @typescript-eslint/parser@latest
13. Would you like to install them now? Yes
14. Which package manager do you want to use? npm (doesn't matter)


And after you will have
`ESLint: Missing file extension for "./test2"(import/extensions)`

Because of:
https://github.com/airbnb/javascript/blob/master/packages/eslint-config-airbnb-base/rules/imports.js#L139

How to fix:
1. Delete `airbnb` from eslint config
2. Add `airbnb-typescript`
