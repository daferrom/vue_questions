// What are directives in Vue ?
/*
Directives provides an easy way to extend the HTML components with new attributes and tags.
Directives intention is to reuse logic that involves low-level DOM access on plain elements.

There are built-in directives in vue for common use cases:
  v-show - toggles the element's visibility
  v-if - conditionally render an element or a template fragment
  v-else - the else block of the v-if
  v-for renders the element or template block multiple times based on the source data
*/

<script setup>

const listNames = ['Diego', 'Alejandro', 'Ferro', 'Martinez']

</script>

<template>
    <h3 v-for="name in listNames">
      <li>{{name }}</li>
    </h3>
</template>