<template>
  <div>
    <h3>Event Caller</h3>
    <p>Oh, that's nice. It's gotten {{ clickCountedValue }} clicks!</p>
  </div>
</template>

<script>
// Import the EventBus.
import { EventBus } from '../event-bus.js';

export default {
  data () {
    return {
      clickCountedValue: 0,
    }
  },
  mounted() {
    EventBus.$on('gotClicked', (clickCount) => {
      this.clickCountedValue = clickCount;
    });
  },
};
</script>
