<template>
  <qrcode-scanner
    :qrbox="250" 
    :fps="10" 
    style="width: 500px;"
    @result="onScan"
  />
</template>

<script>
import QrcodeScanner from './components/QrcodeScanner.vue'

export default {
  name: 'App',
  components: {
    QrcodeScanner
  },
  methods: {
    onScan (decodedText, decodedResult) {
      console.log(decodedText, decodedResult)
    }
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
  margin-top: 60px;
}
</style>
