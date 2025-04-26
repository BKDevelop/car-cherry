<template>
  <v-container>
    <div v-for="trip in trips" :key="trip.id">
      <Trip :trip="trip" />
    </div>
  </v-container>
</template>

<script lang="ts" setup>
  const trips = [
    {
      id: 1,
      name: 'Trip to Berlin',
      startDate: '2023-10-01T10:00:00',
      endDate: '2023-10-05T18:00:00',
      kilometers: 500,
    },
    {
      id: 2,
      name: 'Trip to Munich',
      startDate: '2023-11-01T09:00:00',
      endDate: '2023-11-03T17:00:00',
      kilometers: 300,
    },
    {
      id: 3,
      name: 'Trip to Dresden',
      startDate: '2023-12-01T08:00:00',
      endDate: '2023-12-02T16:00:00',
      kilometers: 200,
    },
  ];
</script>
