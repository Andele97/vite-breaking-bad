<script>

import {store} from '../data/store'

export default {
  name: 'AppSearch',
  data(){
    return{
      store,
    }
  },
  methods: {
    reset(){
      store.characterToSearch = '';
      store.categoryToSearch= '';
      this.$emit('startSearch')
    }
  }
}
</script>

<template>
  <div class="container d-flex align-items-baseline">
    <input v-model="store.characterToSearch" type="text" placeholder="Search">
    <select v-model="store.categoryToSearch" class="form-select form-select-sm" aria-label=".form-select-sm example">
      <option value="" selected>Select category</option>
      <option value="breaking bad">Breaking Bad</option>
      <option value="better call saul">Better Call Saul</option>
    </select>
    <button
    @click="$emit('startSearch')"
    class="btn btn-primary first" type="submit">Search</button>
    <button @click="reset()" class="btn btn-primary" type="submit">Reset</button>
  </div>  

</template>

<style lang="scss" scoped>

  input{
    height: 35px;
    border-radius: 5px;
  }

  select{
    width: 140px;
    margin: 20px;
  }

  button:first-of-type{
    background-color: #52687e;
    margin-right: 15px;
  }

  .isActive{
    background-color: #52687e;
  }

  button{
    background-color: rgb(179, 23, 23);
    border: none;
  }

  button:hover:last-of-type{
    background-color: red ;
  }

</style>