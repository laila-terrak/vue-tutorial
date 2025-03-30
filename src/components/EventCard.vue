<script setup>
defineProps({
  events: {
    type: Object,
    required: true,
  },
})

function eventDetails(event) {
  console.log(event.title)
  console.log(event.time)
  console.log(event.date)
  console.log(event.location)
  console.log(event.description)
}
</script>

<template>
  <div class="event-container" v-for="event in events" :id="event.id" @click="eventDetails(event)">
    <h2>{{ event.title }}</h2>
    <p>@ {{ event.time }} on {{ event.date }}</p>
  </div>
</template>

<style scoped>
.event-container {
  max-width: 300px;
  text-align: center;
  padding: 20px;
  margin: auto;
  margin-bottom: 20px;
  border: 1px solid var(--color-border);
  cursor: pointer;
}

h2 {
  padding: 10px;
}
</style>
