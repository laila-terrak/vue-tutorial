<script setup>
defineProps({
  events: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <div class="event-container" v-for="event in events">
    <h2>{{ event.title }}</h2>
    <p>{{ event.time }} on {{ event.date }} @ {{ event.location }}</p>
    <p>{{ event.decription }}</p>
  </div>
</template>

<style scoped>
.event-container {
  max-width: 100%;
  text-align: center;
  padding: 20px;
  margin: auto;
  margin-bottom: 20px;
  cursor: pointer;
}

h2 {
  padding: 10px;
}
</style>
