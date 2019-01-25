<template>
  <div id="app">
    <ul class="items">
      <li class="item" v-for="(item,index) in pinyin" :key="item">
        <i>{{item}}</i>
        <i>{{hanzi[index]}}</i>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data(){
    return{
      pinyin:['b','p','m','f','d','t','n','l','g','k','h','j','q','x','zh','ch','sh','r','z','c','s','y','w'],
      hanzi:['玻','坡','摸','佛','的','特','呢','了','哥','科','喝','机','妻','西','知','吃','诗','日','资','次','思','衣','屋']
    }
  }
}
</script>


<style>
*{
  list-style: none;
}
.items{
  display: flex;
  max-width: 1000px;
  flex-wrap: wrap;
}
.item{
  text-align: center;
  background-color: rgb(212, 52, 31);
  width: 20%;
  height: 4rem;
  margin-right: 2px;
  margin-top: 20px;
  display: flex;
  flex-direction: column;
}
.item i{
  height: 50%;
  line-height: 200%;
  font-style: normal;
}
#app {
  font-family: '微软雅黑', Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
