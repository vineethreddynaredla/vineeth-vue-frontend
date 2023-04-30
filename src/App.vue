<template>
 <div class="container">
    <MyHeader titleName="TOP FIVE INDIAN RESTAURENTS WITH BAR" 
      details ="Information about restaurents and their popular dish availability" />
    <MyRestaurentDetails :restaurents="restaurents"/>
    <MyAbout About=" Extra details about other restaurents"/>

 </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyRestaurentDetails from './components/MyRestaurentDetails.vue'
import MyAbout from './components/MyAbout.vue'


export default{
name:'App',
components: {
  MyHeader,
  MyRestaurentDetails,
  MyAbout

},

data(){
    return {
      restaurents: [],
      isHidden: false
    }
  },
  methods: {

      async fetchRestaurent(){
         const res= await fetch("https://naredlavineeth.onrender.com/api")
         const data= await res.json()
          console.log(data, data.restaurents)
         return data.restaurents
      }

  },

  async created(){
    this.restaurents = await this.fetchRestaurent()
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
.container {
  max-width: 600px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid rgb(107, 81, 81);
  padding: 30px;
  border-radius: 5px;
  background-color:#b2af61;
}

div{
  margin-bottom: 0.5em;
}
</style>
