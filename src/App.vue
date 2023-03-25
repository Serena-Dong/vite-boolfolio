<script>
import axios from 'axios';
import AppMain from './components/AppMain.vue';
import AppHeader from './components/AppHeader.vue';
import { store } from './data/store.js';

const apiBaseUri = 'http://127.0.0.1:8001/api';

export default {
  name: 'App',
  components: { AppHeader, AppMain },
  data: () => ({
    store,
  }),
  methods: {
    fetchProject() {
      axios.get(apiBaseUri + '/projects').then(res => {
        store.projects = res.data;
      }).catch(err => {
        console.log(err)
      })
    }
  },
  created() {
    this.fetchProject();
  }
}


</script>

<template>
  <AppHeader></AppHeader>
  <AppMain></AppMain>
</template>

<style lang="scss">
@use './assets/sass/style.scss';
</style>
