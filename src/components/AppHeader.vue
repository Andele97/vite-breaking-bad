<script>
export default {
  name: 'AppHeader'
}
</script>

<template>
  
    <div class="container-fluid">
      <header>
        <div class="logo">
          <img src="../assets/img/Breaking_Bad_logo.svg" alt="">
        </div>
        <h1></h1>
      </header>        
    </div>

</template>

<style lang="scss" scoped>

  header {
    height: 60px;
    padding: 15px;
    .logo{
      height: 60px;
      img{
        height: 100%;
      }
    }
  }

</style>