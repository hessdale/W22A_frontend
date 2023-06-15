<template>
    <div>
    <input type="text" placeholder="ID" >
    <button>Delete candy</button>
    </div>
</template>

<script>

import axios from "axios"
    export default {
        name:'DeleteCandy',
        mounted () {
            axios.request({
                url:"http://127.0.0.1:5000/api/candy",
                method:"GET"
            }).then(response =>{
                console.log(response)
            }).catch(failure =>{
                console.log(failure)
            })
        },
    }
</script>

<style scoped>

</style>