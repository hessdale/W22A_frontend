<template>
    <div>
    <h2>Delete Candy By ID</h2>
    <!--input for id and button to call delete function-->
    <input type="text" placeholder="ID" ref="id_input">
    <button @click="delete_candy">Delete candy</button>
    </div>
</template>

<script>

import axios from "axios"

    export default {
        
       methods: {
        //delete candy function
        delete_candy() {
            //takes id from form and sends axios request with parsed value
            let id_value = this.$refs[`id_input`].value
            axios.request({
                url:"http://127.0.0.1:5000/api/candy",
                method:"DELETE",
                data:{
                    id:JSON.parse(id_value)
                }
            }).then(response =>{
                console.log(response)
            }).catch(failure =>{
                console.log(failure)
            })
        }
       },
    }
</script>

<style scoped>

</style>