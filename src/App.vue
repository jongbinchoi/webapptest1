<template>
    <div id ="wrap">
      <header>
        <a class="logo" href="App.vue">
          <img src="./assets/로고1.png" height="100px">
      
        </a>
        <nav>
          <ul class="nav-items">
            <li><a href="App.vue"><i class="fa-regular fa-user"></i></a></li>
            <li><a href="App.vue"><i class="fa-solid fa-bars"></i></a></li>
          </ul>
        </nav>
      </header>
    </div>
    <div class="banner" >
      <img src="./assets/배너.png" alt="배너사진" class="bnnersize"  >
    </div>

    <div class="container">
      <div class="menubar">
        <p class="menubarfont"> 대상자별 (혜택/복지)</p>
       
      </div>
      <div class="menu">
        <div class="image-container">

          <div class="sectioncolumn">
          <a target="_self" href="#"> <!--target="_self"현재 창에서 열음 -->
            <img src="./assets/노인장애인.png" alt="노인/장애인" style="width: 35%;"> 
            <p class="menutext">노인/장애인</p>
          </a>
        </div>

          <div class="vertical-line"></div>

          <div class="sectioncolumn">
          <a target="_self" href="#">
            <img src="./assets/기초수급자.png" alt="기초수급자" style="width: 26%;"  >
            <p class="menutext">기초수급자</p>
          </a>
          </div>
          <div class="vertical-line"></div>

          <div class="sectioncolumn"> 
          <a target="_self" href="#">
            <img src="./assets/임산부.png" alt="임산부" style="width: 28%;">
            <p class="menutext">임산부</p>
          </a>
          </div>
        
        </div>
        
    </div>
  </div>
  </template>
  
  <script>
  
  
  </script>
  
  <style>
 *{ /* *전체 스타일에 적용하겠다. */
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  }
  
  header{
    width: 100%;
    height: 100px;
    z-index: 2000; /*쌓임 순서*/
    background-color: #fff;
    box-shadow: 0 5px 2px rgba(0, 0, 0, 0.05), 0 1px 0 rgba(0, 0, 0, 0.05);
  }
  
  li{
    list-style: none;/*정렬 되지 않은 태그라서 앞에 점이 붙어서 없애주겠다.*/
  }
  
  a{
    text-decoration: none;/*a태그가 텍스트일 때 항상 밑줄이 붙어서 없애줘야함.*/
  }
  
  nav{
    float: right;
  }
  
  .logo{
    display:inline-block;/*inline-block 크기설정가능해짐*/
    height: 100px;
    margin: 12px 0 12px 50px;
  }
  
  .logo > img { height: 80px; }
  
  .nav-items > li {
    display: inline-block;
  }
  
  .nav-items > li > a {
    line-height: 100px;
    padding-right: 50px;
    color: rgba(0, 0, 0, 0.4);
    font-size:25px;
  }
  
  .nav-items > li > a:hover {/*a:ho*/
    color: rgba(0, 0, 0, 0.8);
  }

  .banner{
    text-align: center;
    width: 100%;
    height: 25%;
    position: fixed;
    top:135px;
    left: 0;
    
  }


  .bnnersize{
    width: 80%;
    height: 100%;
    
  }

  .container{
    display:flex; /*한줄 다쓸꺼라고 정의, 보통 가로설정됨*/
    position: absolute;
    top:390px;
  }
  .menubar{
    background-color:#9EBDF8;
    height:200px;
    width: 450px;
    border-top-right-radius: 10px; /*둥근모서리*/
    border-bottom-right-radius: 10px; /*둥근모서리*/
    z-index: 500;
    display: flex;
    justify-content: center; /*속성은 요소들을 가로축 정렬*/
    align-items:center; /*속성은 요소들을 세로축 정렬*/
  }

.menubarfont{
  font-size: 30px;
  font-weight:bold;
}

.menu{
    background: rgba(0, 0, 0, 0.08);/*0~255(R,B,G,투명도)*/
    height:200px;
    width: 1500px;
    position: relative;
    right:10px;
    display: flex;
    align-content: center;
  }
.sectioncolumn{
  flex-grow: 1;/*여백을 채워줌*/
  display: flex;
  flex-direction:column;
  align-items: center;
}

.menutext{
  text-align: center;
  color: black;
  font-weight:bold;
  position: relative;
  bottom: 170px;
}
.image-container{
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 100%;
  }

.image-container img {/*뒤에 img는 모든 이미지에 해당됨.*/
  margin: 179px; /* 이미지 간격을 조정하려면 여기서 마진 값을 조정합니다 */
}

.vertical-line {
  width: 0.09em;
  height: 70%;
  background-color: silver; /* 구분선의 색상을 원하는 색으로 변경할 수 있습니다 */
}
  </style>