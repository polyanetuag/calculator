<template>
  <button 
  class="button"
  @click="$emit('onClick', label)"
   :class="{ double, triple, operation }">
    
    {{ label }}
  </button>
</template>

<script>
export default {
  props: {
    label: {},
    operation: {type: Boolean },
    double: {type: Boolean },
    triple: {type: Boolean }
  }
}
</script>

<style>
  :root {
    --bg-button: #f0f0f0;
    --border-button: solid 1px #888;
  }

  .button {
    font-size: 1.4rem;
    background: var(--bg-button);
    border: none;
    border-right: var(--border-button);
    border-bottom: var(--border-button);
    outline: none;
  }

  .button:active {
    background: #ccc;
  }

  .button.double {
    grid-column: span 2;
  }

  .button.triple {
    grid-column: span 3;
  }

  .button.operation {
    background: #fa8231;
    color: #fff;
  }

  .button.operation:active {
    background: #fa8231cc;
  }
</style>