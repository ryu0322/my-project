<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <SelfMessage msg="あぱぱぱぱぱ" />
    <LeftMessage msg="あたたたたた" />
    <MessageForm />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import SelfMessage from './components/SelfMessage.vue'
import LeftMessage from './components/LeftMessage.vue'
import MessageForm from './components/MessageForm.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    SelfMessage,
    LeftMessage,
    MessageForm
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
