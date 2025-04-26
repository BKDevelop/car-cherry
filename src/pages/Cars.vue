<template>
  <v-container>
    <div v-for="car in cars" :key="car.id">
      <Car :car="car" />
    </div>
  </v-container>
</template>

<script lang="ts" setup>
  const cars = [
    {
      id: 1,
      name: 'BMW M3',
      location: 'Berlin',
      image: 'https://images.pexels.com/photos/30433744/pexels-photo-30433744/free-photo-of-leuchtend-orangefarbener-bmw-m3-in-izmir-ausgestellt.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1',
    },
    {
      id: 2,
      name: 'Audi A4',
      location: 'Munich',
      image: 'https://images.pexels.com/photos/11213779/pexels-photo-11213779.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1',
    },
    {
      id: 3,
      name: 'Barkas B1000',
      location: 'Dresden',
      image: 'https://images.pexels.com/photos/10990952/pexels-photo-10990952.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1',
    },
  ];
</script>
