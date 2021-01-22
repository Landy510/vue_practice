<template>
  <div id="app">
    <img src="./assets/logo.png">
    <HelloWorld/>
    <button class="btn btn-danger">按鈕</button>  
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  created(){
    this.$http.get('https://randomuser.me/api/').then((reponse) =>{
      console.log(reponse.data);
    })
  }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";
</style>
