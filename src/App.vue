<template>
  <div class="modal1-1" v-if="모달창1 == true">
    <div class="modal1-2">
      <h4>지역별 배달량</h4>
      <p></p>
      <img src="./assets/bm1.jpg">
      <button @click="모달창1 = false">닫기</button>
    </div>
  </div>

  <div class="modal2-1" v-if="모달창2 == true">
    <div class="modal2-2">
      <h4>지역별 평균배달 소요시간</h4>
      <div class="menu-2">
        <a @click="지역1 = true, 지역2 = false, 지역3 = false, 지역4 = false, 지역5 = false">경기도 의정부시</a>
        <a @click="지역2 = true, 지역1 = false, 지역3 = false, 지역4 = false, 지역5 = false">제주도 서귀포시</a>
        <a @click="지역3 = true, 지역1 = false, 지역2 = false, 지역4 = false, 지역5 = false">서울시 영등포구</a>
        <a @click="지역4 = true, 지역1 = false, 지역2 = false, 지역3 = false, 지역5 = false">경기도 시흥시</a>
        <a @click="지역5 = true, 지역1 = false, 지역2 = false, 지역3 = false, 지역4 = false">경상북도 안동시</a>
      </div>
      <img src="./assets/bm2-1.jpg" v-if="지역1 == true">
      <img src="./assets/bm2-2.jpg" v-if="지역2 == true">
      <img src="./assets/bm2-3.jpg" v-if="지역3 == true">
      <img src="./assets/bm2-4.jpg" v-if="지역4 == true">
      <img src="./assets/bm2-5.jpg" v-if="지역5 == true">
      <button @click="모달창2 = false, 지역1 = false, 지역2 = false, 지역3 = false, 지역4 = false, 지역5 = false">닫기</button>
    </div>
  </div>

  <div style="font-size:40px">배달의민족
    <h5 style="font-size:20px">관리자</h5>
  </div>

  <div class="menu-1">
    <a @click="모달창1 = true">지역별 배달량</a>
    <a @click="모달창2 = true">지역별 평균 배달 소요시간</a>
  </div>

  <div>
    <img src="./assets/bmrider.jpg">
  </div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return {
      모달창1 : false, 모달창2 : false,
      지역1 : false, 지역2 : false, 지역3 : false, 지역4 : false, 지역5 : false,
    }
  },
  components: {
    
  }
}
</script>

<style>
* {
  font-family: 'BMHANNAPro';
}
body {
  background-color: #19BDB5;
  margin: 0
}
div {
  box-sizing: border-box;
}
.modal1-1 {
  width: 100%; height: 100%;
  background: rgba(0,0,0,0.5);
  position: fixed; padding: 20px;
}
.modal1-2 {
  width: 100%; background: white;
  border-radius: 8px;
  padding: 20px;
}
.modal2-1 {
  width: 100%; height: 100%;
  background: rgba(0,0,0,0.5);
  position: fixed; padding: 20px;
}
.modal2-2 {
  width: 100%; background: white;
  border-radius: 8px;
  padding: 20px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
}

.menu-1 {
  color: white;
  background-color: #40E0D0;
  padding: 15px;
  border-radius: 10px;
}

.menu-1 a {
  font-size: 20px;
  padding: 50px;
}

.menu-2 {
  background-color: #A0D9D9;
  padding: 10px;
  border-radius: 10px;
}

.menu-2 a {
  font-size: 20px;
  padding: 50px;
}

@font-face {
font-family: 'BMHANNAPro';
src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_seven@1.0/BMHANNAPro.woff') format('woff');
font-weight: normal;
font-style: normal;
}
</style>
