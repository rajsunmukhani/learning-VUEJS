<template>
    <h1>Hello {{x}}</h1>
    <h1>Your Mobile Number is {{ getNumber() }}</h1>
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
                getNumber : function(){
                    return '7987'
                }
            }
        }
    }
</script>