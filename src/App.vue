<template>

  <div class="black-bg" v-if="모달창열렸니 == true">
    <div class="white-bg">
      <h4>상세페이지임</h4>
      <p>상세페이지 내용임</p>
      <button @click="모달창열렸니 = false">닫기</button>
    </div>
  </div>



  <div class="menu">
    <a v-for="a in 메뉴들" :key="a">{{a}}</a>
  </div>



<div>
  <a v-for="(원룸,index) in 6" :key="index">
  <img :src="원룸들[index].image" class="room-img">
  <h4 @click="모달창열렸니 = true">{{원룸들[index].title}}</h4>
  <p>{{원룸들[index].price}}</p>
  </a>
</div>




</template>

<script>

//import 작명 from './components/oneroom.js'; //작명부분에 자유롭게 작명 가능 , js같은 확장자 생략가능
import data from './assets/oneroom.js';


export default {
  name: 'App',
  data(){//데이터 바인딩을 위한 데이터 보관함.
    return{
      원룸들 : data,
      모달창열렸니 : false,
      신고수 : [0,0,0],
      renthome : ['신촌원룸', '신림원룸', '천호동원룸'],
      메뉴들 : ['Home', 'Shop', 'About'], //자료형(3) 만큼 반복문반복,메뉴생성에 필요한 정보들을 data란에 저장
    }
  },
  methods : {
    increase(){
      this.신고수[0]+=1;
    },
    

  },
  components: {
 
  }
}
</script>

<style>
body {
  margin : 0
}
div {
  box-sizing: border-box;
}
.black-bg{
  width: 100%; height: 100%;
  background: rgba(0,0,0,0.5);
  position: fixed; padding: 20px;
}
.white-bg {
  width: 100%; background: white;
  border-radius: 8px;
  padding: 20px;
}


.room-img{
  width: 100%;
  margin-top: 40px;
}


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a{
  color: white;
  padding: 10px;
}
</style>
