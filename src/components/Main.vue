<template>
  <div class="main">
    <h1>Эта вабще классное прилажене</h1>
    <h1>{{ user }}</h1>
  </div>
</template>

<script>
let tg = window.Telegram.WebApp; //получаем объект webapp телеграма 

tg.expand(); //расширяем на все окно  

export default {
  name: 'Main',
  data () {
    return {
      user: null
    }
  },
  mounted () {
    this.user = tg.initDataUnsafe.user
    console.log(this.user)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.main {

}
</style>
