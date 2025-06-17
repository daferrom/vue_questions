// What are slots on Vue //
/* Is another way can pass content to its children.
However , instead of JS values,
Slots allows to pass in template content or fragments to another component.
*/

For example:

// FancyHeader component wraps the template content passed by the parent component in an h1 tag and adds some custom styling:

// The use of fancy header passing the content //
<FancyHeader>
  Hello! <!-- slot content-->
</FancyHeader>

// The fancy Header template //
<h1 class="fancy-header">
  <slot></slot> <!-- slot outlet-->
</h1>



