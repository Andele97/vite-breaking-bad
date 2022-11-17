<script>

import AppHeader from './components/AppHeader.vue'
import AppSearch from './components/AppSearch.vue'
import AppMain from './components/AppMain.vue'
import CharacterList from './components/CharacterList.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    AppSearch,
    AppMain,
    CharacterList
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