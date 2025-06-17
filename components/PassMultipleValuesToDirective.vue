// How do you pass ultiple values to a directive

/*
A directive accepts any valid JavaScript expression including objects

Therefore, JS literal object could be used when a directive require multiple values.

*/

<div v-user="{ name: 'Bob',  age: 30 }"></div>

app.directive('user', (el, binding) => {
  console.log(binding.value.name) // => "Bob"
  console.log(binding.value.age) // => "30"
})

// composition API

<!-- Paso del objeto a la directiva -->
<h4 v-my-directive="{ name: 'Alan', age: 'Turing' }"></h4>


app.directive('my-directive', {
  mounted(el, binding) {
    // binding.value será: { foo: 'uno', bar: 'dos' }
    console.log(binding.value.name); // "Bob"
    console.log(binding.value.age); // "age"
  }
});