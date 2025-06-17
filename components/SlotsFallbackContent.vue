// The fallback or default contetn for a slot.
It is the content which will be render in the case that no content passed to the child.

Adds flexibility allowing the content passing as an option.

The fallback content is defined  in hthe template within slot tags.

// Imagine this is the GreetingComponent

<div class="greeting">
  <slot>
     <h2>Hi User</h2> <!-- fallback content -->
  </slot>
</div>

// 1.  When a Template content is passed:

<GreetingComponent>
  <h1>Whats up?</h1>
</GreetingComponent>

<!-- will generate the following output -->
<div class="greeting">
  <h1>Whats up?</h1>
</div>

// 2. When no template is passed in

<GreetingComponent></GreetingComponent>

<!-- will generate the following output -->
<div class="greeting">
  <h2>Hi</h2>
</div>