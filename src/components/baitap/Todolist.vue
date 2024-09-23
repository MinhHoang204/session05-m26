<template>
  <div class="todo-app">
    <h1>To-Do List</h1>
    <input v-model="newJob" ref="jobInput" placeholder="Enter your job" />
    <button @click="addJob">Add Job</button>
    <ul>
      <li v-for="(job, index) in jobs" :key="index">
        <input type="checkbox" v-model="job.completed" @change="updateJob(index)" />
        <span :class="{ completed: job.completed }">{{ job.name }}</span>
        <button @click="confirmDelete(index)">Delete</button>
      </li>
    </ul>
    <p>Số công việc hoàn thành: {{ completedJobs }}/{{ jobs.length }} công việc</p>
    <div v-if="showModal" class="modal">
      <p>Bạn có chắc chắn muốn xóa công việc này?</p>
      <button @click="deleteJob">Xóa</button>
      <button @click="showModal = false">Hủy</button>
    </div>
  </div>
</template>

<script>
import { ref, reactive, computed, onMounted } from 'vue';

export default {
  name: 'ToDoApp',
  setup() {
    const newJob = ref('');
    const jobs = reactive(JSON.parse(localStorage.getItem('jobs') || '[]'));
    const showModal = ref(false);
    const jobToDelete = ref(null);

    const addJob = () => {
      if (newJob.value.trim()) {
        jobs.push({ name: newJob.value, completed: false });
        newJob.value = '';
        saveJobs();
      }
    };

    const updateJob = (index) => {
      jobs[index].completed = !jobs[index].completed;
      saveJobs();
    };

    const confirmDelete = (index) => {
      jobToDelete.value = index;
      showModal.value = true;
    };

    const deleteJob = () => {
      if (jobToDelete.value !== null) {
        jobs.splice(jobToDelete.value, 1);
        jobToDelete.value = null;
        showModal.value = false;
        saveJobs();
      }
    };

    const saveJobs = () => {
      localStorage.setItem('jobs', JSON.stringify(jobs));
    };

    const completedJobs = computed(() => jobs.filter(job => job.completed).length);

    onMounted(() => {
      saveJobs();
    });

    return {
      newJob,
      jobs,
      showModal,
      jobToDelete,
      addJob,
      updateJob,
      confirmDelete,
      deleteJob,
      completedJobs,
    };
  },
};
</script>

<style>
.todo-app {
  max-width: 400px;
  margin: 0 auto;
  text-align: center;
}

.completed {
  text-decoration: line-through;
}

.modal {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: white;
  padding: 20px;
  border: 1px solid #ccc;
}
</style>
