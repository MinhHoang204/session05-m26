<template>
    <div>
      <!-- Button để thay đổi giá trị của isShow -->
      <button @click="isShow = true">Click me</button>
  
      <!-- Hiển thị nội dung khi isShow là true -->
      <p v-if="isShow">Rikkei Education</p>
    </div>
</template>
  
<script>
  export default {
    data() {
      return {
        isShow: false, // Biến kiểu boolean, giá trị khởi tạo là false
      };
    },
  };
</script>
  
<style scoped>
  button {
    padding: 10px 20px;
    background-color: #007bff;
    color: white;
    border: none;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #0056b3;
  }
  
  p {
    font-size: 18px;
    color: #333;
    margin-top: 10px;
  }
</style>
  