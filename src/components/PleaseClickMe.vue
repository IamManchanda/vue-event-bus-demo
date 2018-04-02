<template>
  <a @click="emitGlobalClickEvent()">Click Me</a>
</template>

<script>
import { EventBus } from '../event-bus.js';

export default {
  data() {
    return {
      clickCount: 0
    }
  },
  methods: {
    emitGlobalClickEvent() {
      this.clickCount++;
      EventBus.$emit('gotClicked', this.clickCount);
    }
  }
}
</script>
