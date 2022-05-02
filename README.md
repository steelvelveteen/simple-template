# A frontend template setup with Typescript and CSS (Maybe Tailwind CSS)

## Configuring ESLint airbnb and Prettier for a non-reactjs project

**Prettier** A code formatter used here for Typescript

**NOTE:** Format on Save must be set on VSCode and configured to prettier

Packages:

1. `npm install --save-dev eslint eslint-config-airbnb-base @typescript-eslint/eslint-plugin @typescript-eslint/parser`

2. `npm install --save-dev prettier`. Optionally `npm install --save-dev eslint-plugin-jest`

3. To configure Prettier to work with ESLint: `npm install --save-dev eslint-config-prettier eslint-plugin-prettier eslint-plugin-import`

4. eslintrc.json must know where to find the `tsconfig.json` configuration file. This is set in the `parserOptions` section: `"project": ["tsconfig.json"]`

5. Add scripts to format and lint: `"format": "prettier --write src/**/*.ts{,x}"` and `"lint": "tsc --noEmit && eslint src/**/*.ts{,x}"`

6. Add a `.prettierignore` file to exclude build, dist and public directories

7. To run this simple project run `npm run watch` that will keep an eye on the .ts files and at the same time run `npm run dev` which is the nodemon watching the changes on the compiled javascript file
