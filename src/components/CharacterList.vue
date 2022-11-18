<script>

import { store } from '../data/store';
import CharacterCard from './CharacterCard.vue'
import AppLoading from './AppLoading.vue'

export default {
  name: 'CharacterList',
  components: {
    CharacterCard,
    AppLoading
  },
  data(){
    return{
      store
    }
  }
}
</script>

<template>
  
  <main class="container">
    <div class="found">
      Found 62 characters
    </div>
    <div v-if="store.isLoaded" class="row d-flex justify-content-center">
    <CharacterCard
    v-for="character in store.charactersListData" 
    :key="character.id" 
    :character="character"/>
    </div>
    <div v-else>
      <AppLoading />
    </div>

  </main>

</template>

<style lang="scss" scoped>

@use '../styles/general.scss' as *;

  .container{
    background-color: white;
    min-height: 100vh;
    padding: 20px;
    .found{
      background-color: black;
      color: white;
      padding: 15px;
      font-weight: bold;
      margin: 20px;
    }
  }

</style>