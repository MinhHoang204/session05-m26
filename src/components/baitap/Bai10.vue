<template>
    <div>
      <!-- Nút để random số -->
      <button @click="addRandomNumber">Random number</button>
  
      <!-- Hiển thị mảng các số -->
      <div>
        <h3>Các số đã thêm:</h3>
        <ul>
          <li v-for="(number, index) in numbers" :key="index">{{ number }}</li>
        </ul>
      </div>
    </div>
</template>
  
<script>
  export default {
    data() {
      return {
        // Mảng rỗng để lưu các số ngẫu nhiên
        numbers: [],
      };
    },
    methods: {
      // Hàm tạo ra số ngẫu nhiên và thêm vào mảng
      addRandomNumber() {
        const randomNumber = Math.floor(Math.random() * 100) + 1; // Số ngẫu nhiên từ 1 đến 100
        this.numbers.push(randomNumber); // Thêm số vào mảng
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
  
  ul {
    list-style-type: none;
    padding: 0;
  }
  
  li {
    margin: 5px 0;
    padding: 5px;
    background-color: #f0f0f0;
    border: 1px solid #ddd;
  }
</style>
  