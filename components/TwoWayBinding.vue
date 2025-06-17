// How do you create ttwo way bindings in Vue ?

/* Two way binding system is one of the most powerful useful features of Vue.
  Vue simplifies user input handling and synchronization by the using of v-model directive
  The v-model directive updates the model whenever the template changes and updates the template when the model changes
*/


// In Options API
export default {
  data() {
    return {
      name: 'Bob'
    }
  },
  template: `
    <h2>Hello {{ name }}</h2>
  <input v-model="name"/>
  `
}

// Other example 

<!-- CustomInput.vue -->
<script>
export default {
  props: ['modelValue'],
  emits: ['update:modelValue']
}
</script>

<template>
  <input
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
  />
</template>