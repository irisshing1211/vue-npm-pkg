# vue-npm-pkg
 This repo is a vue component libary package for **npm**.
 
 In this project, I also try to install `eslint` and `bootstrap-vue`
 
 ## Preparation / What you will need
 1. install [vue-sfc-rollup](https://www.npmjs.com/package/vue-sfc-rollup)
  `npm install -g vue-sfc-rollup`
 2. you must have an npm account
 3. If you want to create a private package, your must have a **npm pro / npm teams / GitHub Enterprise** account
 ## Getting start
 1. After installed `vue-sfc-rollup` in globla, cd to the root directory then run `sfc-init` to init the project
 2. It'll need you to answer some question:
```
Vue2 or Vue3? Vue2
Is Single component or Library? Library
What's the npm name? your-pkg-name
Prefer Javascript or Typescript? Javascript
And the location? //this'll auto fill: ./your pkg name
```
3. Then install packages that you'll need.
4. To add code to `main.js` or `app.js`, go to `/dev/serve.js`

## Create your components
1. Go to `/src/lib-components` to create your component. I create `LargeBtn.vue` here.
2. After completed you componet, go to `/src/lib-components/index.js` and type `export { default as LargeBtn }from './LargeBtn.vue';
## Try your component
1. Go to `/dev/serve.vue`, just add your componet code inside the `<div id="app">`
`<large-btn txt="12345" />`
2. Then you can use `npm run serve` to try out your componet
#### Ref
[YouTube - Create and Publish your first Vue Component Library on NPM](https://www.youtube.com/watch?v=0WqB6XwBCLc)

[How to Create and Publish a Vue Component Library](https://www.freecodecamp.org/news/how-to-create-and-publish-a-vue-component-library/)
