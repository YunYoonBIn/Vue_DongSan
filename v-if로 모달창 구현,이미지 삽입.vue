<template>
  <div class="black_bg" v-if="모달창_닫힘 == flase">
    <div class="white_bg">
      <h4>상세페이지</h4>
      <button class="button_flase" @click="모달창_닫힘 = true">닫기</button>
      <p>상세페이지 내용</p>
    </div>
  </div>

  <div class="menu">
    <a v-for="(a,i) in menu" :key="i">{{a}}</a>
  </div>

  
  <div>
     <img src="./assets/room0.jpg" alt="룸0" class="room_img">
     <h4 @click="모달창_닫힘 = flase">{{products[0]}}</h4>
     <p>{{price1}} 만원</p>
     <button @click="신고수[0] ++ ">허위매물신고</button> <span>신고수 : {{신고수[0]}} </span>
   </div>
  
  <div>
     <img src="./assets/room1.jpg" alt="룸1" class="room_img">
     <h4 @click="모달창_닫힘 = flase"> {{products[1]}}</h4>
     <p>{{price2}} 만원</p>
     <button @click="신고수[1] ++ ">허위매물신고</button> <span>신고수 : {{신고수[1]}} </span>
  </div>

  <div>
     <img src="./assets/room2.jpg" alt="룸2" class="room_img">
     <h4 @click="모달창_닫힘 = flase">{{products[2]}}</h4>
     <p>{{price3}} 만원</p>
     <button @click="신고수[2] ++ ">허위매물신고</button> <span>신고수 : {{신고수[2]}} </span>
  </div>

</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      모달창_닫힘 : true,
      price1 : 60,
      price2 : 70,
      price3 : 80,
      신고수 : [0,0,0],
      products : ['역삼동원룸' , '천호동원룸' , '마포구원룸'],
      menu : ['Home' , 'Shop' , 'About'],
    }
  },
  methods : {
     increase() {
       this.신고수 =+ 1;   
     }
  },

  components: {
   
  }
}
</script>

<style>

body{
  margin: 0
}

div{
  box-sizing: border-box;
}

.black_bg{
  width: 100%; height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  position: fixed;
  padding: 20px;
}

.white_bg{
  width: 30%;
  position: relative;
  left: 35%; 
  background-color: white;
  border-radius: 8px;
  padding: 20px;
  top: 10%;
}

.button_flase {
  border-radius: 5px;
  position: absolute;
  left: 90%;
  bottom: 75%;

}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  background-color: darkslateblue;
  border-radius: 5px;
  padding: 15px;
}

.menu a {
  color: white;
  padding: 30px;
  text-decoration: none;
  text-align: center;
}

.room_img {
  width: 40%;
  margin-top: 40px;
}
</style>
