<template>
  <div class="container">
    
    <Header siteName="Top 6 World wonders" 
      authorName="Madhavi Kuchipudi"/>

    <wonderbox :wonders="wonders"  />

  </div>
</template>
<script>





import Header from './components/Header.vue'
import wonderbox from './components/wonderbox.vue'



export default {
  name: 'App',
  components: {
    
    Header,
    wonderbox
  },

  data(){
    return {
      wonders: []
    }
  },
  methods: {
  

      async fetchwonders(){
        //  const res= await fetch('http://localhost:5555/wonders')
        const res= await fetch('https://madhavibackendproject.herokuapp.com/api')
         const data= await res.json()
        console.log(data)
         return data
      }

  },

  async created(){
    this.wonders = await this.fetchwonders()
    console.log(this.wonders);
  }
}
</script>



<style>


@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 500px;
  border: 0.3em solid red;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;
}



</style>


