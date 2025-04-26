<template>
  <div class="car-card">
    <img alt="Car Image" class="car-image" :src="car.image">
    <div class="car-details">
      <h2 class="car-name">{{ car.name }}</h2>
      <p class="car-location">{{ car.location }}</p>
      <button class="book-button" @click="bookCar">Book</button>
    </div>
  </div>
</template>
<script lang="ts" setup>
  import { defineProps } from 'vue';
  const props = defineProps({
    car: {
      type: Object,
      required: true,
    },
  });
  const bookCar = () => {
    alert(`Car ${props.car.name} booked!`);
  };
</script>

<style scoped>
  .car-image {
    width: 100%;
    height: auto;
    max-width: 300px;
    max-height: 200px;
  }
  .car-card {
    display: flex;
    flex-direction: column;
    align-items: center;
    border: 1px solid;
    border-radius: 8px;
    padding: 16px;
    margin: 16px;
  }
  .car-details {
    text-align: center;
  }
  .car-name {
    font-size: 1.5em;
    margin: 0;
  }
  .car-location {
    font-size: 1em;
  }
  .book-button {
    border: solid 1px #007BFF;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1em;
  }
</style>
