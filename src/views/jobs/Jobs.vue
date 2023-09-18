<template>
  <h1>Jobs</h1>
  <div v-for="job in jobs" :key="job.id">
    <router-link :to="{ name: 'JobDetails', params: { id: job.id } }">
      <h2>{{ job.title }}</h2>
    </router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        { title: "J1", id: 1, details: "111111" },
        { title: "J2", id: 2, details: "222222" },
        { title: "J3", id: 3, details: "333333" },
      ],
    };
  },
};
</script>

<style></style>
