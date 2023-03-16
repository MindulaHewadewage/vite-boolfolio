<script>
import ProjectsList from '../components/projects/ProjectsList.vue';
import axios from 'axios';
const apiBaseUrl = 'http://127.0.0.1:8000/api/'

export default {
    name: 'HomePage',
    components: { ProjectsList },
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
}
</script>


<template>
    <main class="container">
        <ProjectsList :projects="projects" />

    </main>
</template> 


<style></style>