// How do you access the root instance in Vue ?

/*

1. Inside a component:

You can access the root instance using:

this.$root

For example:

mounted() {
  console.log(this.$root)
}

This provides access to properties and methods defined in the root instance

2. From the Vue app (Vue 3 Composition API)

In Vue 3 with the Composition API, there in no `this` so you use getCurrentInstance()

*/

import { getCurrentInstance, onMounted }

onMounted(()=>{
  const internalInstance = getCurrentInstance();
  const root = internalInstance.appContext.app
  console.log(root)
})

3. When creating the root Instance

In Vue 2:


const app = new Vue({
  data() {
    return {
      message: 'Hello'
    }
  }
}).$mount('#app')

In Vue 3:

const app = createApp(App)
app.
