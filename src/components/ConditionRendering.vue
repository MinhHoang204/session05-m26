<template>
    <div>
        <!-- v-if: được sử dụng khi khỏi lệnh cho có 1 điều kiện -->
        <h1 v-if="isShow">Hiển thị phần tử</h1>
        <h1 v-else>Ẩn phần tử</h1>
    
        <button @click="handleToggle">Toggle</button>
        
        <!-- v-if và v-else: được sử dụng khi khối lệnh có 2 điều kiện -->

        <h1 v-if="age >= 18">Đủ tuổi thi</h1>
        <h1 v-else>Chưa đủ tuổi thi</h1>
        <h1>Tuổi: {{ age }}</h1>
    
        <button @click="handleIncreaseAge">Tăng tuổi</button>
        <button v-on:click="handleDecreaseAge">Giảm tuổi</button>
        
        <!-- v-if, v-else-if, v-else: được sử dụng khi khối lệnh có từ 3 điều kiện trở lên -->
        <h1 v-if="role === 'admin'" >Quyền admin</h1>
        <h1 v-else-if="role === 'user'">Quyền user</h1>
        <h1 v-else-if="role === 'edit'">Quyền edit</h1>
        <h1 v-else>Quyền other</h1>

        <!-- v-show: Hiển thị dữ liệu có điều kiện, tuy nhiên là dữ liệu đó không bị xóa khỏi DOM mà nó chỉ bị ẩn đi thông qua display: none -->
        <h1 v-show="isShowForm">Form content</h1> 
    </div>
</template>

<script setup>
import { ref } from 'vue';

  const isShow = ref(true);
  // Tạo ra các biến phản ứng
  const age = ref(0);
  const role = ref("creator")
  const isShowForm = ref(true);

  const handleToggle = () => {
    isShow.value = !isShow.value;
  }
  
  // Tạo 1 biến tuổi. Nếu tuổi trên 18 thì sẽ hiển thị "Đủ tuổi thi", ngược lại: "Chưa đủ tuổi thi"

  // Hàm tăng tuổi
  const handleIncreaseAge = () => {
    // Cập nhật lại giá trị của biến age
    age.value++;
  }
  
  // Hàm giảm tuổi
  const handleDecreaseAge = () => {
    // Cập nhật lại giá trị của biến age
    age.value--;
  };
  
  // Tạo một biến "role" có giá trị có thể là: admin, user, edit, other
</script>

<style></style>