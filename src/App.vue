<template>
  <div id="app">
    <MainPage />
  </div>
</template>

<script>
import MainPage from './components/MainPage.vue'

export default {
  name: 'App',
  components: {
    MainPage
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Cuprum&family=Silkscreen&display=swap');
#app {
  font-family: 'Cuprum', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: #141414;
}
body::-webkit-scrollbar {
  width: 6px;
}
body::-webkit-scrollbar-track {
  background: #222222;
}
body::-webkit-scrollbar-thumb {
  background-color: #33614a;
  border-radius: 20px;
  border: none;
}
</style>
