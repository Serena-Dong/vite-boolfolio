<script>
export default {
    name: 'ProjectCard',
    props: { project: Object }
}
</script>
<template>
    <h3>{{ project.title }}
    </h3>
    <img v-if="project.image_url" src={{ project.image_url }} alt="">
</template>
<style></style>