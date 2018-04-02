<template>
  <div id="app">
    <h1>Event Bus</h1>
    <please-click-me />
    <event-caller />
  </div>
</template>

<script>
import PleaseClickMe from './components/PleaseClickMe.vue';
import EventCaller from './components/EventCaller.vue'

export default {
  name: 'app',
  components: {
    'please-click-me': PleaseClickMe,
    'event-caller': EventCaller,
  },
  data () {
    return {
    }
  }
}
</script>

<style lang="scss">
</style>
