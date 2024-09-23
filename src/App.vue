<script setup>
// import ConditionRendering from './components/ConditionRendering.vue';
// import ListRendering from './components/ListRendering.vue';
import Bai1 from './components/baitap/Bai1.vue';
import Bai2 from './components/baitap/Bai2.vue';
import Bai3 from './components/baitap/Bai3.vue';
import Bai4 from './components/baitap/Bai4.vue';
import Bai5 from './components/baitap/Bai5.vue';
import Bai6 from './components/baitap/Bai6.vue';
import Bai7 from './components/baitap/Bai7.vue';
import Bai8 from './components/baitap/Bai8.vue';
import Todolist from './components/baitap/Todolist.vue';
</script>

<template>
  <!-- <ConditionRendering></ConditionRendering> -->
  <!-- <ListRendering></ListRendering> -->
  <Todolist></Todolist>
  <Bai1></Bai1>
  <Bai2></Bai2>
  <Bai3></Bai3>
  <Bai4></Bai4>
  <Bai5></Bai5>
  <Bai6></Bai6>
  <Bai7></Bai7>
  <Bai8></Bai8>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
