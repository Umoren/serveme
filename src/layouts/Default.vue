<template>
  <div class="container mx-auto px-4 py-4 ">
    <header class="">
      <Navbar />
    </header>
    
     
    <slot/>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
import Navbar from '~/components/Navbar'
export default {
  name: 'default',
  components: {
    Navbar
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Karla&family=Poppins&display=swap');
body {
  font-family: 'Poppins', 'Karla', sans-serif;
  font-weight: 400;
  line-height: 1.2;
  margin:0;
  padding:0;
  line-height: 1.5;
  background-color: #F9F7F1;
  color: #000000;
}



</style>
