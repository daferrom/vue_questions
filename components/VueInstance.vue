/*
A Vue instance is the core object that powers Vue Application.
It serves as the connection between your data(reactive state ) and the DOM (HTML)

When a Vue instance is created , you tell Vue how to render the UI and
how to respond to data changes

What's Vue Instance ?

In Vue 2:

its created using the new Vue() constructor.
It controls a portion of the DOM , defines data, methods , and lifecycle hooks.

new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }
})


In Vue 3:

Its created using createApp() from vue
The result is called an application instance,
and it is used to mount the app and register global configurations:
(components, directives, plugins, etc)

// main.js
import { createApp } from 'vue'
import App from './App.vue'

// Create the app instance
const app = createApp(App)

// Mount it to a DOM element
app.mount('#app')


<!-- index.html -->
<div id="app"></div>


*/
