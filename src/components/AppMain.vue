<script>
import { store } from '../data/store.js'
export default {
    name: 'AppMain',
    data: () => ({
        store
    })
};
</script>

<template>
    <main>
        <div class="container">
            <h3 v-for="project in store.projects">{{ project.title }}
            </h3>
        </div>
    </main>
</template>

<style lang="scss" scoped>
main {
    background-color: rgb(40, 40, 40);
}
</style>
