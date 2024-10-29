<template>
    <h1>Hello {{x}}</h1>
    <h1>Your Mobile Number is {{ getNumber().number }}</h1>
</template>

<style scoped>
    h1{
        color: red;
    }
</style>

<script>
    export default {
        name : 'HelloComponent',
        data() {
            return{
                x : 'Raj',
                number : '9223'
            }
        },
        methods : {
            getNumber(){
                return {
                    email : 'raj@gmail.com',
                    number : this.number
                }
            }
        }
    }
</script>