<template>
  <JobList :jobs="jobs"/>
</template>
  <script lang="ts">
import { defineComponent, reactive, ref } from "vue";
import JobList from "./components/JobList.vue";
import type Job from "./types/Job";
export default defineComponent({
  name: "App",
  components: { JobList },
  setup() {
    // const state = reactive({
    //   name: "link",
    //   age: 25 as string | number,
    // });
    // const height = ref<number |string>(25);
    // return { ...state, height };
    const jobs = ref<Job[]>([
      { id: "123", location: "Thai Nguyen", salary: 1000000, title: "Worker" },
      { id: "456", location: "Thai Nguyen", salary: 1000000, title: "Worker" },
    ]);
    return {jobs}
  },
});
</script>
  <style scoped>
.read-the-docs {
  color: #888;
}
</style>
  
  