<template>
 <div class="container">
    <MyHeader titleName="MOST VIEWED AND SALED MANGAS" />
    <DetailsOfManga :Mangas="Mangas"/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import DetailsOfManga from './components/DetailsOfManga.vue'


export default{
name:'App',
components: {
  MyHeader,
  DetailsOfManga
},

data(){
    return {
      Mangas: [],
      isHidden: false
    }
  },
  methods: {

      async fetchManga(){
         const res= await fetch("http://localhost:7230/Mangas")
         const data= await res.json()
          console.log(data)
         return data
      }

  },

  async created(){
    this.Mangas = await this.fetchManga()
  }
}
 
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');

.container {
  max-width: 600px;
  margin: 30px auto;
  min-height: 300px;
  border: 0.3em solid rgb(63, 107, 132);
  padding: 30px;
  border-radius: 30px;
  background-color:blanchedalmond;
}
</style>
