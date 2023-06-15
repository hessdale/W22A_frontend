<template>
    <div>
        <article v-for="(candy,i) in candies" :key="i" >
            <img :src="candy[`image_url`]" alt="tasty candy" width="200px">
            <h3>{{ candy['name'] }}</h3>
            <p>{{ candy['description'] }}</p>
        </article>
    </div>
</template>

<script>

import axios from "axios"
    export default {
        data() {
            return {
                candies: undefined
            }
        },
        name:'AllCandy',
        mounted () {
            axios.request({
                url:"http://127.0.0.1:5000/api/candy",
                method:"GET"
            }).then(response =>{
                console.log(response)
                this.candies=response.data
            }).catch(failure =>{
                console.log(failure)
            })
        },
    }
</script>

<style scoped>

</style>