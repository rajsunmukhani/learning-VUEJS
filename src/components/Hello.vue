<template>
    <h1>Loop in Vue JS</h1>
    <ul>
        <li v-for="item in items" :key="item">{{item}}</li>
    </ul>
    <ul>
        <li v-for="user in users" :key="user.email">
            Name : {{ user.name }}
            <br>
            Email : {{ user.email }}
            <br>
            Age : {{ user.age }}
            <br>
            <br>
        </li>
    </ul>
</template>

<style scoped>
   
</style>

<script>
    export default {
        name : 'HelloComponent',
        data() {
            return {
                items: ['Apple', 'Banana', 'Cherry', 'Dragonfruit', 'Elderberry', 'Fig', 'Grape', 'Honeydew', 'Iced Tea', 'Jackfruit', 'Kiwifruit', 'Lemon', 'Mango', 'Nectarine', 'Orange', 'Papaya', 'Quince', 'Raspberry', 'Strawberry', 'Tangerine'],
                users : [{
                    name: 'John Doe',
                    age: 30,
                    email: 'john.doe@example.com'
                },{
                    name: 'Jane Doe',
                    age: 25,
                    email: 'jane.doe@example.com'
                },{
                    name: 'Bob Smith',
                    age: 35,
                    email: 'bob.smith@example.com'
                }]
            }
        }
    }
</script>