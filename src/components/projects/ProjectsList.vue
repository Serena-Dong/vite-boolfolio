<script>
import { store } from '../../data/store.js'
import ProjectCard from './ProjectCard.vue'

export default {
    name: 'ProjectList',
    components: { ProjectCard },
    data: () => ({
        store
    })
}
</script>
<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-3 h-50 m-2" v-for="project in store.projects">
                <ProjectCard :project="project"></ProjectCard>
            </div>
        </div>
    </div>
</template>
<style></style>