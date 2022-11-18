<script>
export default {
  name: 'AppSearch'
}
</script>

<template>
  <div class="container">
    <select class="form-select form-select-sm" aria-label=".form-select-sm example">
      <option selected>Select category</option>
      <option value="1">One</option>
      <option value="2">Two</option>
      <option value="3">Three</option>
    </select>
  </div>  

</template>

<style lang="scss" scoped>

  select{
    width: 140px;
    margin-bottom: 20px;
  }

</style>