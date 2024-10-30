<template>
    <h1>Getting the value of input Feild</h1>

    <input type="email" v-model="email" placeholder="Enter email" name="" id="">
    <br><br>

    <input type="password" v-model="password" placeholder="Enter Password" name="" id="">
    <br><br>

    <button type="button" v-on:click="getData()">Get values</button>
</template>

<style scoped>
   
</style>

<script>
    export default {
        name : 'HelloComponent',
        data(){
            return {
                email : null,
                password : null
            }
        },
        methods : {
            getData(){
                console.log('values :', this.email, this.password);
            }
        }
    }
</script>