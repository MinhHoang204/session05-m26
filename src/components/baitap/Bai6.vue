<template>
    <div>
      <h3>Danh sách các số thỏa mãn điều kiện:</h3>
      <div>
        <!-- Render các số thỏa mãn điều kiện -->
        <span v-for="(num, index) in filteredNumbers" :key="index">
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
        array: [5, 12, 15, 22, 9, 18, 25, 30, 7, 33],
      };
    },
    computed: {
      // Lọc các số chia hết cho 3 và 5
      filteredNumbers() {
        return this.array.filter((num) => num % 3 === 0 && num % 5 === 0);
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
  