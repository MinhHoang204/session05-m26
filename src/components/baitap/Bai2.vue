<template>
    <div>
      <!-- Button để thay đổi giá trị của isShow -->
      <button @click="toggleShow">{{ isShow ? 'Hiện' : 'Ẩn' }}</button>
    </div>
</template>
  
<script>
  export default {
    data() {
      return {
        isShow: false, // Biến kiểu boolean, giá trị khởi tạo là false
      };
    },
    methods: {
      // Phương thức để chuyển đổi giá trị isShow
      toggleShow() {
        this.isShow = !this.isShow;
      },
    },
  };
</script>
  
<style scoped>
  button {
    padding: 10px 20px;
    background-color: #28a745;
    color: white;
    border: none;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #218838;
  }
</style>
  