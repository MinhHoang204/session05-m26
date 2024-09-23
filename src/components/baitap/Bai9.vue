<template>
    <div>
      <!-- Nút Random gender -->
      <button @click="randomGender">Random gender</button>
  
      <!-- Hiển thị giới tính -->
      <div>
        <h3>Giới tính hiện tại:</h3>
        <p>{{ currentGender }}</p>
      </div>
    </div>
</template>
  
<script>
  export default {
    data() {
      return {
        // Mảng chứa các giới tính
        genders: ['Nam', 'Nữ', 'Khác'],
        // Giới tính mặc định là Nam
        currentGender: 'Nam',
      };
    },
    methods: {
      // Hàm để chọn ngẫu nhiên một giới tính từ mảng
      randomGender() {
        const randomIndex = Math.floor(Math.random() * this.genders.length);
        this.currentGender = this.genders[randomIndex];
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
  