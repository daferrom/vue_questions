// What are props in Vue ?

Props are custom attributes you can register in a component.
They are used to pass data from a parent component to its child components. When a value is passed as a prop attribute, 
it becomes a property on the component instance and can be accessed using the `this` keyword.

export default {
  props [ 'foo'],
  created() {
    console.log(this.foo)
  }
}