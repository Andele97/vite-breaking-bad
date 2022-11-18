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
  methods:{
    getCharacters(){
      store.isLoaded = false;
    axios.get(store.apiUrl)
    .then( result => {
      store.charactersListData = result.data
      store.isLoaded = true;
   })
   .catch(error => {
      console.log(error)
   })
  }
  },
  mounted(){
    this.getCharacters()
  }
}
</script>

<template>
  <AppHeader title="Breaking Bad Api"/>
  <AppSearch />
  <CharacterList />
</template>

<style lang="scss">

  @use './styles/general';

</style>