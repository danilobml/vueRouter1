<template>
  <div>
    <h1>Job Details</h1>
    <h2>{{ details }}</h2>
  </div>
</template>

<script>
import jobsData from "@/data/jobs.json";
import { useRoute } from "vue-router";
export default {
  props: ["id"],
  setup() {
    const route = useRoute();
    const foundId = Number(route.params.id);
    const foundJob = jobsData.find((x) => x.id === foundId);
    const details = foundJob.details;
    return { details };
  },
};
</script>

<style scoped></style>
