<template>
  <div>
    <h2>Add Commuting Record</h2>
    <form @submit.prevent="addCommuteRecord">
      <label>
        Distance (km):
        <input v-model="distance" type="number" min="0" />
      </label>
      <label>
        Select Means of Commuting:
        <select v-model="selectedMeans">
          <option value="0.0">Select...</option>
          <option value="0.02">Foot</option>
          <option value="0.03">Bike</option>
          <option value="0.04">Train</option>
          <option value="0.1">Car</option>
        </select>
      </label>
      <button type="submit" :disabled="selectedMeans === '0.0'">Add Commuting Record</button>
    </form>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const distance = ref(0);
const selectedMeans = ref('0.0');

const addCommuteRecord = () => {
  // Validate input
  if (isNaN(distance.value) || distance.value <= 0 || selectedMeans.value === '0.0') {
    alert('Please enter valid distance and select means of commuting.');
    return;
  }

  // Demo: Simulate storing the commuting record
  const commuteRecord = {
    distance: distance.value,
    means: selectedMeans.value,
    timestamp: new Date(),
  };

  // Dispatch an action to store the commuting record (you can replace this with actual API call or store action)
  $store.dispatch('employee/addCommuteRecord', commuteRecord);

  // Clear the form
  distance.value = 0;
  selectedMeans.value = '0.0';

  alert('Commute record added successfully!');
};
</script>
