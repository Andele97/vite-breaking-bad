<script>
import axios from 'axios';
import { store } from './data/store';

import AppHeader from './components/AppHeader.vue'
import AppSearch from './components/AppSearch.vue'
import CharacterList from './components/CharacterList.vue'

export default {
  name: 'App',
  data(){
    return{
      store
    }
  },
  components: {
    AppHeader,
    AppSearch,
    CharacterList
  },
  methods: {
    
  }
}
</script>

<template>
  <AppHeader />
  <AppSearch />
  <AppMain />
</template>

<style lang="scss">

  @use './styles/general';

</style>