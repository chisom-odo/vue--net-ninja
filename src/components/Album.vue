<template>
<div class="album--border">
    <!-- <hr /> -->
    <div>
        <label>Artist:</label>
        <p>{{ artist }}</p>
    </div>
    <div>
        <label>Album Number:</label>
        <p>{{ album }} {{ albumNumber }}</p>
    </div>
    <div>
        <label>Release Date:</label>
        <p>{{ FormattedDate }}</p>
    </div>
    <div>
        <label>Good Album:</label>
        <p>{{ goodAlbum ? 'Yes':'No' }}</p>
    </div>
</div>
</template>

<script>
    export default {
        name:"Album",
        props:{
            artist:{
                type:String,
                required:true
            },
            album:{
                type:String,
                default:"No idea"
            },
            albumNumber:{
                type:Number,
            },
            rawDate:{
                type:Date,
                default:Date.now(),
            },
            goodAlbum:{
                type:Boolean,
            }
        },
        computed:{
            FormattedDate(){
                return new Date(this.rawDate).toLocaleString('en-US',{
                    month:'long',
                    day:'numeric',
                    year:'numeric'
                })
            }
        },
        data(){
            return{

            }
        },
        
}
</script>

<style scoped>
.album--border{
    border:3px solid grey;
    border-radius: 6px;
    /* background-color: red; */
    width:70%;
    margin-top:36px;
    padding-block:50px;
    margin-inline:auto;

}
</style>
