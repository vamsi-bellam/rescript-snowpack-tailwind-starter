
### Starting Application

1. Run `npm run start` - to start rescript compiler in watch mode for generating js files
2. Run `npm run server` - to serve the files through snowpack config


### Creating starter app

1. create a folder and run `npm init`(Answer the questions after init)
2. Then install the following dependencies and dev dependencies using npm

```
#deps
npm i @rescript/react react react-dom

#dev deps
npm i --save-dev rescript
```

3. Install snowpack using `npm i --save-dev snowpack` as a dev dependency and then run `npx snowpack` to generate snowpack config.
4. Install tailwind, postcss and autoprefixer (`npm install --dev tailwindcss postcss autoprefixer`) and run `npx tailwindcss init` to generate tailwind config.
5. Create a file named `index.css` with following content

```
/* index.css */
@tailwind base;
@tailwind components;
@tailwind utilities;
```
then link the stylesheet in index.html (`<link rel="stylesheet" href="index.css" />`)

6. Create a file named `postcss.config.js` with the following content

```
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
}
```
7. Install snowpack postcss plugin(`npm i --save-dev @snowpack/plugin-postcss`) for using postcss(a CSS transpiler) and add this `"@snowpack/plugin-postcss"` under plugins in `snopack.config.js`