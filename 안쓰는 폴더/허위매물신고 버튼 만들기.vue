<template>
  
  <div class="menu">
    <a v-for="(a,i) in menu" :key="i">{{a}}</a>
  </div>


  <img alt="Vue logo" src="./assets/logo.png">
  
  <div>
     <h4>{{products[0]}}</h4>
     <p>{{price1}} 만원</p>
     <button @click="신고수 += 1">허위매물신고</button> <span>신고수 : {{신고수}} </span>
   </div>
  
  <div>
     <h4>{{products[1]}}</h4>
     <p>{{price2}} 만원</p>
  </div>

  <div>
     <h4>{{products[2]}}</h4>
     <p>{{price3}} 만원</p>
  </div>

</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      price1 : 60,
      price2 : 70,
      price3 : 80,
      신고수 : 0,
      products : ['역삼동원룸' , '천호동원룸' , '마포구원룸'],
      menu : ['Home' , 'Shop' , 'About'],
    }
  },
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
</style>
