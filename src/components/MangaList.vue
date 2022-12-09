<template>

        <h2>{{Manga.title}}</h2>
        <div class = "NAZEER">
            <p>
                <ul>
                   <u>Year of Release:</u> {{Manga.yearOfRelease}}<br>
                   <u>Author's Name:</u> {{Manga.AuthorName}}<br>
                   <u>genre:</u> {{Manga.genre}}<br>
                   <u>IMDB Rating:</u> {{Manga.IMDBRating}}<br>
                </ul>
            </p>
        </div>
</template>

<script>

export default{
    name: 'MangaList',
    props:{
        Manga: Array
    }  
}
</script>

<style scoped>



h2{
    margin: 2px;
}

div{
    background-color: rgb(119, 221, 228);
    color: #d81159;
    padding: 1em;
}

ul
{

}
</style>