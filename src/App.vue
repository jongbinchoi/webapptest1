<template>
  <div class="container">
    <div class="line"></div>
    <div class="logo-container">
      <img src="./assets/로고1.png" class="rogo-img">
    </div>
  </div>



 
</template>

<script>


export default {
  name: 'App',
  components: {

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 1px;
}

.container{
  position: relative;
 
}

.logo-container{
position: absolute;
top: -1px;
left:0;
}

.rogo-img{
  width: 10em;
 

}
.line{
  position: absolute;
  top: 70px;
  left: 0;
  background: black;
  width: 100%;
  height: 1px;
  
}


</style>