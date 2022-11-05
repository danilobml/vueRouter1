<template>
  <div>
    <h1>Jobs:</h1>
    <div v-for="job in jobs" :key="job.id">
      <router-link
        :to="{
          name: 'jobDetails',
          params: { id: job.id },
        }"
        >{{ job.title }}</router-link
      >
    </div>
  </div>
</template>

<script>
import jobs from "@/data/jobs.json";
export default {
  data() {
    return {
      jobs: jobs,
    };
  },
};
</script>

<style scoped></style>
