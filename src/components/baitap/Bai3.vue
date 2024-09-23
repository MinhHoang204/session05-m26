<template>
    <div>
      <!-- Kiểm tra và hiển thị quyền của user dựa vào giá trị của userRole -->
      <p v-if="userRole === 'admin'">
        Quyền hạn của bạn là: <strong>Admin</strong>
      </p>
      <p v-if="userRole === 'user'">
        Quyền hạn của bạn là: <strong>User</strong>
      </p>
      <p v-if="userRole === 'guest'">
        Quyền hạn của bạn là: <strong>Guest</strong>
      </p>
    </div>
</template>
  
<script>
  export default {
    data() {
      return {
        userRole: 'guest', // Giá trị của userRole có thể là 'admin', 'user', hoặc 'guest'
      };
    },
  };
</script>
  
<style scoped>
  /* CSS cho component */
  p {
    font-size: 18px;
    color: #333;
  }
  
  strong {
    font-weight: bold;
  }
</style>
  