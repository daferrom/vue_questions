// How do you create components in Vue

There are two ways to create components in Vue:
// depends on the build step
// 1. When the build step is used, we typically use a single file component (SFC) with a .vue extension
// like this:

<script>
export default {
  data() {
    return {
      name: 'Bob'
    }
  }
}
</script>

<template>
  <h1>Hello {{ name }}</h1>
</template>

// 2. When the build step is not used, we can create components using the Vue.component 
as a plain Javascript object containg Vue-specific options like this:

export default {
  data() {
    return {
      name 'Diego'
    }
  }
  template: `
    <h1> Hello {{ Diego }}</h1>
  `
}
