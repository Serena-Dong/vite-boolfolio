<script>
import ProjectsList from './projects/ProjectsList.vue';
export default {
    name: 'AppMain',
    components: { ProjectsList }
};
</script>

<template>
    <main>
        <ProjectsList></ProjectsList>
    </main>
</template>

<style lang="scss" scoped>
main {
    background-color: rgb(40, 40, 40);
    min-height: 90vh;
}
</style>
