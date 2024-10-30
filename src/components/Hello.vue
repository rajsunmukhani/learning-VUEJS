<template>
    <h1>Getting the value of Checkboxes and Radio buttons</h1>

    <br><br>
    <label for="Node">Node</label> <input v-model="technology" value="Node" type="checkbox" name="" id="Node">
    <label for="Java">Java</label> <input v-model="technology" value="Java" type="checkbox" name="" id="Java">
    <label for="Javascript">Javascript</label> <input v-model="technology" value="Javascript" type="checkbox" name="" id="Javascript">
    
    <h3>Technologies: {{ technology }} </h3>


    <br><br>
    <label for="Student">Student</label> <input v-model="who" value="Student" type="radio" name="identity" id="Student">
    <label for="Fresher">Fresher</label> <input v-model="who" value="Fresher" type="radio" name="identity" id="Fresher">
    <label for="working">Working prfessional</label> <input v-model="who" value="Working Professional" type="radio" name="identity" id="working">
    
    <h3>You are -  {{ who }} </h3>



</template>

<style scoped>
   
</style>

<script>
    export default {
        name : 'HelloComponent',
        data(){
            return {
                technology : [],
                who : null
            }
        }
    }
</script>