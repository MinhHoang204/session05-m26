<template>
    <div>
      <h3>Các số chẵn từ mảng:</h3>
      <div>
        <!-- Render các số chẵn -->
        <span v-for="(num, index) in evenNumbers" :key="index">
          {{ num }} &nbsp;
        </span>
      </div>
    </div>
</template>
  
<script>
  export default {
    data() {
      return {
        // Mảng các số nguyên bất kỳ
        array: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
      };
    },
    computed: {
      // Lọc các số chẵn từ mảng
      evenNumbers() {
        return this.array.filter((num) => num % 2 === 0);
      },
    },
  };
</script>
  
<style scoped>
  h3 {
    font-size: 18px;
    color: #333;
  }
  
  span {
    font-size: 20px;
    margin-right: 10px;
  }
</style>
  