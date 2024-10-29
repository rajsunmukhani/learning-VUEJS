<template>
    <h1>Hello {{x}}</h1>
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
                x : 'Raj'
            }
        }
    }
</script>