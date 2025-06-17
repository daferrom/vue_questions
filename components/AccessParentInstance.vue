// How do you access parent Instance ?

Depends on the Version and API you're using

Vue 2 (Options API)

1. Inside a component

<script>

  this.$parent

</script>

This gives direct access to the parent instance. including its data , methods, computed, properties, etc.

<script>

  mounted() {
    console.log(this.$parent) // Logs the parent component instance
  }

</script>


Vue 3 (Options API)

<script>

  mounted() {
    console.log(this.$parent) // Logs the parent component instance
  }

</script>

Vue 3 (Composition API)
you use getCurrentInstance

<script>

onMounted(()=>{
  const internalInstance = getCurrentInstance();
  const parent = internalInstance.parent;
  console.log(parent) // Internal component instance of the parent
})

</script>

🧠 Best Practices
Directly accessing this.$parent or instance.parent:

❌ Not recommended for most use cases.

✅ Prefer using:

Props to send data down from parent to child.

Events ($emit) to send data from child to parent.

provide / inject for deep or indirect component communication (especially in Vue 3).