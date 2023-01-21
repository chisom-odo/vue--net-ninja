<template>
  <!-- When you are trying to pass in individual data from parent to child component -->
  <!--<Album :artist="album.artist" :album="album.album" /> -->
<Album v-bind="album"/>
</template>
<script>
import Album from './Album.vue'
    export default{
        name:"Parent",
        data(){
            return{
              // rawDate: new Date(1986 ,2, 3),
              album:{
                artist:"Chisom",
                album:"Master of puppets",
                albumNumber:"3",
                rawDate: new Date(1986 ,2, 3),
                goodAlbum:false
              }  
            }

        },
        methods:{
            
        },
        components:{
          Album  
        }
    }
</script>