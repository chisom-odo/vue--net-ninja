<template>
<label >
    {{ label }}
    <input type="text" v-model="inputValue"/>
</label>
</template>


<!-- if you want to make the variables at the child component to be in sync with the parent variable -->
<script>
export default{
    name:'CustomInput',
    data(){
        return{
            inputValue:'',
        }
    },
    props:['label']
}
</script>
<style scoped>

input{
    display: flex;
    margin: 0 auto;
    flex-direction: column;
    
}

</style>