<script>
export default {
    name: 'ProjectCard',
    props: { project: Object }
}
</script>


<template>
    <section id="project-card">
        <div class="card my-3 mx-3" style="width: 18rem;height: 18rem;">
            <div class="card-body">
                <h5 class="card-title">{{ project.title }}</h5>
                <p class="card-text">{{ project.content }}</p>
                <div class="buttons d-flex justify-content-end">
                    <button class="btn btn-primary ">Details</button>
                </div>

            </div>
        </div>
    </section>
</template> 


<style></style>