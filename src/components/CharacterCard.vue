<script>
export default {
  name: 'CharacterCard',
  props:{
    character: Object
  }
}
</script>

<template>

    <div class="ap-cards col-2">
      <div class="image">
        <img :src="character.img" :alt="character.name" >
        <div class="middle">
          {{character.nickname}}
        </div>
      </div>
      <div class="text">
        <h4>{{character.name}}</h4>
        <p class="text-white-50 m-0 mt-4">{{character.category}}</p>
        <span class="text-white-50">{{character.status}}</span>
      </div>
    </div>

</template>

<style lang="scss" scoped>

@use '../styles/partials/vars' as *;

.image{
  width: 100%;
  height: 69%;
  position: relative;
}

img{
  width: 100%;
  height: 99%;
}

.middle{
  transition: .5s ease;
  opacity: 0;
  position: absolute;
  bottom: 0px;
  left: 50%;
  transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  text-align: center;
  text-transform: uppercase;
  color: white;
  font-weight: bold;
  font-size: 1.4em;
  text-shadow: 2px 2px 4px black;
}

.ap-cards:hover .middle {
  opacity: 1;
}

.ap-cards{
      background-color: rgb(46, 58, 70);
      width: 210px;
      height: 430px;
      padding: 15px;
      margin-right: 20px;
      margin-bottom: 10px;
      position: relative;
      .text{
        text-align: center;
        h4{
          color: white;
          font-weight: bold;
          text-transform: uppercase;
          font-size: 1em;
          margin-top: 10px;
        }
      }
    }
  .ap-cards:hover{
    background-color: rgba(46, 58, 70, 0.906);
  }  

</style>