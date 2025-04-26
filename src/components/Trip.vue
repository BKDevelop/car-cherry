// card with startdate with time, enddate with time and kilometers
<template>
  <div class="trip-card">
    <h2 class="trip-name">{{ trip.name }}</h2>
    <p class="trip-start-date">Startdatum: {{ trip.startDate }}</p>
    <p class="trip-end-date">Enddatum: {{ trip.endDate }}</p>
    <p class="trip-kilometers">Kilometer: {{ trip.kilometers }}</p>
  </div>
</template>
<script lang="ts" setup>
  import { defineProps } from 'vue';
  const props = defineProps({
    trip: {
      type: Object,
      required: true,
    },
  });
</script>
<style scoped>
  .trip-card {
    display: flex;
    flex-direction: column;
    align-items: center;
    border: 1px solid;
    border-radius: 8px;
    padding: 16px;
    margin: 16px;
  }
  .trip-name {
    font-size: 1.5em;
    margin: 0;
  }
  .trip-start-date,
  .trip-end-date,
  .trip-kilometers {
    font-size: 1em;
  }
</style>
