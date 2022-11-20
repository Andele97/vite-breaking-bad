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
      axios.get(store.apiUrl, {
        params:{
          name: store.characterToSearch,
          category: store.categoryToSearch
        }
      })
      .then( result => {
      store.charactersListData = result.data
      store.isLoaded = true;
   })
   .catch(error => {
      store.charactersListData = [];
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
  <AppSearch @startSearch="getCharacters()" />
  <CharacterList />
</template>

<style lang="scss">

  @use './styles/general';

</style>