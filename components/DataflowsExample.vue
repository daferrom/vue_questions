// How data flows between conponents in Vue

Vue uses props and events to communicate between component 

Data passes from a parent component to a child one. using a prop.
Then the prop becomes a property on the child component instance.
The following snippet shows us how the parent component passes a prop named `title` to the child component.

<ChildComponent title="Hello!" />

// The children components use an event to communicate back to their parents. the parent can listen to these events by attachig an event listener to any event the child emits.

The snippet below shows how the child component emits a childevent when the button is clicked and how the parent listens to the event by attaching a callback to the event.

<!-- parent listening to the event -->
<ChildComponent @child-event="callback" />

<!-- child.vue -->
<button @click="$emit('child-event')">click me</button>