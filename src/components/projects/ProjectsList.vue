<script>
import ProjectCard from './ProjectCard.vue';

export default {
    name: 'ProjectsList',
    components: { ProjectCard },
    props: { projects: Array }
}
</script>


<template>
    <section id="projects-list">
        <div class="d-flex flex-wrap">
            <ProjectCard v-for="project in projects" :key="project.id" :project="project" />
        </div>
    </section>
</template> 


<style></style>