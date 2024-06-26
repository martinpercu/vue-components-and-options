# Components Options and API Compositions

## First steps.
- Start a vue projects with vite.
```sh
npm init vite
```
- Then 
```sh
cd "folder name (same name of project)"
npm install
```
- From now .....
```sh
npm run dev
```
- Something to see is also the command
```sh
vue ui
```
- This is a manager with ui for vue project

## Async Components
- In App.vue will create a const "HelloWorld" using defineAsyncComponent. This will charge in an async way this component. So will first charge the page and then will charge the component.
- I left commented the line 2 where the components is imported directly. (just to see the difference)

## Transicions
- In App.vue create one button with boolean on click. (showed). To switch showed or not a menu.
- New file Menu.vue with a simple menu.
- In App.vue add a new <Menu component with v-show="showed">
- In App template add <transition>. Then inside put the <Menu> Component
- Name the thansition (this case fadeMenu)
- Add styles name starting with fadeMenu + enter or leave + from or active or leave. 
- Check the lines 43 to 50 in App.vue. (App-old-01.vue)


## Teleports
- I left the last App.vue saved as App-old-01.vue.
- In App.vue import a new component "Modal"
- Create the Modal.vue then just add a modal + a button to show it.
- The modal itself in a div. Then all this div inside a <teleport to="body">.
- With this all inside the <teleports> is already moved to the css class body. (check it in the browser inspector.) 

## Lifecycle
- I left the last App.vue saved as App-old-02.vue.
- In App.vue just add : beforeCreate() + created() + mounted()  with a console.log to see what is getting in each moment of the lifecycle of the element App.

## Mixins
- I left the last App.vue saved as App-old-03.vue.
- The mixins is a way to "keep code to use anywhere" something like.
- Create a folder mixins
- Then a js file (this case will be example_01.js + example)
- In App.vue import this file.
- Add it with this format: "mixins: [example01, example02]",
- IMPORTANT if we have the same name variable in the mixin and in the component will use the var from the component.
- The Mixins are really good if we want to do "same something" with several component but is not easy to know what there is in the mixin. (With Vue 3 works much better with options and Composition API)





# Vue 3 + Vite

This template should help get you started developing with Vue 3 in Vite. The template uses Vue 3 `<script setup>` SFCs, check out the [script setup docs](https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup) to learn more.

## Recommended IDE Setup

- [VS Code](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).
