<template>
  <div >
    <Header/>
    <Main/>
    <Footer/>
  
  </div>
</template>

<script>

  import Header from '@/components/Header.vue'
  import Main from '@/components/Main.vue'
  import Footer from '@/components/Footer.vue'

  export default {
    name: 'App',
    components: {
      Header,
      Main,
      Footer,
    }
  }
</script>

<style >
body {
  margin: 0;
  padding: 0;
  background-color: aliceblue;
  font-family: 'Raleway', sans-serif;
font-family: 'Roboto', sans-serif;
}
</style>
