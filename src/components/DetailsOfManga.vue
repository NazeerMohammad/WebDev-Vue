<template>
    <div class="M">
        <div v-for="Manga in Mangas" :key="Manga.id" >     
               <MangaList :Manga="Manga"/>
        </div>
    </div>

</template>

<script>
import MangaList from "./MangaList.vue"
export default {
    name: 'DetailsOfManga',
    components: {
        MangaList
    },
    props:{
        Mangas: Array

    }
}


</script>


<style>
.M{

    background-color:rgb(210, 151, 173);
    border: 5px solid black;
    padding: 1em;
    color: rgb(11, 11, 11);
}

</style>