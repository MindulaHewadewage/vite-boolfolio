<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import AppHeader from './components/projects/ProjectCard.vue';
const apiBaseUrl = 'http://127.0.0.1:8000/api/'
export default {
  name: 'App',
  components: { AppHeader, ProjectCard },
  data: () => ({
    projects: []
  }),
  methods: {
    fetchProjects() {
      axios.get(apiBaseUrl + 'projects').then(res => {
        this.projects = res.data;
      });
    }
  },
  created() {
    this.fetchProjects();
  }
};
</script>



<template>
  <AppHeader />
  <main class="container">
    <ProjectCard />

  </main>
</template>

<style></style>