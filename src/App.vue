<script setup>
import EventBucket from './components/EventBucket.vue'
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup

</script>

<template>
  <event-bucket :events="today">Detta händer idag</event-bucket>
</template>

<script>
export default {
  data: () => {
    return {
      today: [{title: 'bruh', time: '10.10-20.20', desc: 'a little desc'}]
    }    
  }
}
</script>

<style>
body {
  margin: 0;
}
</style>
