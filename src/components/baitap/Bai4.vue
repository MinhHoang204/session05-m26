<template>
    <div>
      <!-- Nút hiển thị thông báo -->
      <button @click="isVisible = true">Hiển thị</button>
      <!-- Nút ẩn thông báo -->
      <button @click="isVisible = false">Ẩn</button>
  
      <!-- Phần tử thông báo -->
      <div v-show="isVisible" class="notification">
        Đây là thông báo của bạn!
      </div>
    </div>
</template>
  
<script>
  export default {
    data() {
      return {
        isVisible: false, // Giá trị mặc định của biến là false
      };
    },
  };
</script>
  
<style scoped>

  button {
    padding: 10px 20px;
    margin-right: 10px;
    background-color: #007bff;
    color: white;
    border: none;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #0056b3;
  }
  
  .notification {
    margin-top: 20px;
    padding: 10px;
    background-color: #f8d7da;
    color: #721c24;
    border: 1px solid #f5c6cb;
    border-radius: 4px;
  }
</style>
  