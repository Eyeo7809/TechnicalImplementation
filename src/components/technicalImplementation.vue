<template>
    <div class="grid-container">
      <!-- Loop through gridItems array to create grid cells -->
      <div v-for="(item, index) in gridItems" :key="index" class="grid-item">
        {{ item }}
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        // Data for grid items
        gridItems: ['Item 1', 'Item 2', 'Item 3', 'Item 4', 'Item 5', 'Item 6'],
      };
    },
  };
  </script>
  
  <style scoped>
  /* Style for grid container */
  .grid-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr); /* 3 columns with equal width */
    gap: 16px; /* Space between items */
    padding: 16px;
  }
  
  /* Style for individual grid items */
  .grid-item {
    background-color: #f0f0f0;
    padding: 20px;
    text-align: center;
    border: 1px solid #ddd;
  }
  </style>
  