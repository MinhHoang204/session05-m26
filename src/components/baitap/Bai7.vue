<template>
    <div>
      <!-- Tạo ba nút button -->
      <button
        v-for="index in 3"
        :key="index"
        :class="{ active: activeIndex === index }"
        @click="setActive(index)"
      >
        Button {{ index }}
      </button>
    </div>
</template>
  
<script>
  export default {
    data() {
      return {
        // Biến activeIndex với giá trị mặc định là 1
        activeIndex: 1,
      };
    },
    methods: {
      // Hàm để cập nhật giá trị của activeIndex khi nhấn button
      setActive(index) {
        this.activeIndex = index;
      },
    },
  };
</script>
  
<style scoped>
  /* Định dạng button */
  button {
    margin: 10px;
    padding: 10px 20px;
    border: 1px solid #ccc;
    background-color: #f4f4f4;
    color: #333;
    cursor: pointer;
  }
  
  /* Thêm class active khi button được chọn */
  .active {
    background-color: red;
    color: #fff;
  }
</style>
  