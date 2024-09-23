<template>
    <div>
      <!-- Nút Tăng dần và Giảm dần -->
      <button @click="sortAscending">Tăng dần</button>
      <button @click="sortDescending">Giảm dần</button>
  
      <!-- Hiển thị mảng số nguyên -->
      <div>
        <h3>Mảng các số nguyên:</h3>
        <p>{{ numbers.join(', ') }}</p>
      </div>
    </div>
</template>
  
<script>
  export default {
    data() {
      return {
        // Mảng các số nguyên
        numbers: [3, 7, 1, 9, 5, 8, 2, 4, 6],
      };
    },
    methods: {
      // Sắp xếp mảng theo thứ tự tăng dần
      sortAscending() {
        this.numbers.sort((a, b) => a - b);
      },
      // Sắp xếp mảng theo thứ tự giảm dần
      sortDescending() {
        this.numbers.sort((a, b) => b - a);
      },
    },
  };
</script>
  
<style scoped>
  button {
    margin: 10px;
    padding: 10px 20px;
    border: 1px solid #ccc;
    background-color: #f4f4f4;
    color: #333;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #ddd;
  }
</style>
  