<script>
export default {
  name: 'AppHeader',
  props:{
    title: String
  }
}
</script>

<template>
  
    <div class="container-fluid p-3">
      <header>
        <div class="logo">
          <img src="../assets/img/Breaking_Bad_logo.svg" alt="">
        </div>
        <h1 class="text-white ml-5">{{title}}</h1>
      </header>        
    </div>

</template>

<style lang="scss" scoped>

  header {
    display: flex;
    .logo{
      height: 60px;
      img{
        height: 100%;
        }
      }
    h1{
      margin-left: 20px;
    }
  }

</style>