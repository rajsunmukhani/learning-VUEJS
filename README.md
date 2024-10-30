## Learning Vue JS.

**What is Vue JS?**

=> Vue JS is javascript framework, basically used to create SPA (Single Page Applications).
=> It is progressive in nature, thuswe are not limited to the provided features only, we can install the third party packages and enhance the efficiency of code as well as out project.
=> Vue Js was basically created by Evan You, an ex google employee, in Feb 2014.
=> Currently we are using the Vue JS 3 version of Vue.

**Installation of Vue JS**

=> Installation can be ignored by just using the cdn of the framework.
=> Otherwise, installation requires Node as well as NPM to get started : 
    We just need to write following command in trerminal and we are ready to go! The commands is as follows : 
        *npm install -g @vue/cli*

    For verification of download simply type "vue" on the terminal.

**Making a folder for VUE JS**

=> Following command undertakes the creation of file for Vue js:
    *vue create foldername*
=> Select the VUE 3, and proceed
=> Get to the folder using *cd foldername*
=> run server as : *npm run serve*

**Understanding File/Folder structure of Vue js**

=> *node_modules :* It contains all the packages which are to be used in the project.
=> *public :* It basically contains the html page as well as we can add the favicon, to use in html page for our project.
=> *src :* This contains the assets, components and main.js file with the main parent component App.vue, of the webiste.
=> *.gitignore :* This file as in react keeps the file names which are not to be uploaded at the time of pushing code to git.
=> *babel.config.js :* It is basically used to convert the data of our code according to the effecient readibility of browser.
=> *package-lock.js :* It contains detailed info. of all the packages named under *package.json*
=> *package.json :* It contains name of all the packages which are required to be downloaded in node_modules for running the code.

**Understanding Vue JS**

=> Basically, the vue js undertakes the production with the help of components, and each component contains following three things :
    *1. Template tag*
    *2. Script Tag*
    *3. Style Tag*

**Code flow in Vue JS**

As per the code flow the first page which takes place to run is main.js, this page basically runs App.vue, imports the data from App.vue and injects the code in html page.

**Adding Extension in Vue JS**

1. vue (syntax highlight for vuejs) *jcbuisson* (or any updated extension of your choice)
2. vue format (a beutify extension for .vue file) *fc_bean*  (or any updated extension of your choice)

**Making our first component**

*Component :* Components are basically the building blocks of a website, which combine together to form a particular web application.
(Chunk of code which basically defins a specific functionality and which can is re-usable in nature.)

**Creating a component**

under the folder src, under component folder create a file named Home.vue with three base tags : template, script and style, as:

<template>
    <h1>Hello component</h1>
</template>

<style></style>

<script>
    export default {
        name : 'HelloComponent'
    }
</script>

and update App.vue as:

<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <Hello />
</template>

<script>
import Hello from './components/Hello.vue'

export default {
  name: 'App',
  components: {
    Hello
  }
}
</script>

<style>

</style>


**Adding CSS to component**

As we add CSS in the child component Hello.vue we can see that it targets all the h1 present in full website and changes the property for all, thus making it css property global.
To avoid this we can simply add a key word *scoped* to the style tag as : 
    *<style scoped></style>*

**Interpolation and dynamic data in VUE**

*Ques :* What is *Interpolation*?
*Ans :* *Interpolation* basically helps the programmer to use the functions, variables or other javascript things in html.To do so, programmer needs to use {{data}} (double curlly braces inside the html of template tag.)

*Ques :* How interpolation works in Vue JS
*Ans :* For making interpolation work in VUE JS we have to define variable, function or method first in script tag under some respective heads, and then we can use them in html present under template tags.

**Making interpolation of variables**

To make the dynamic value of variable visible in html, use data(){} attribute in script, which will return the key value paid of variables, and use the variable in double cursly braces in html as:

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

**Making interpolation for function**

It is mostly similar to variable as :

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

**Passing params in function if needed**

<template>
    <h1>Hello {{x}}</h1>
    <h1>Your Mobile Number is {{ getNumber() }}</h1>
    <h1>Your Email : {{ getEmail('raj@gmail.com') }}</h1>
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
                },
                getEmail : function(email){
                    return email;
                }
            }
        }
    }
</script>


**IMP : In vue JS value prop can be assigned with the value at the time of interpolation also, unlike angular.**

**Methods in VueJS using *this***

To define method we need to use a data property in script named *methods* as:

methods : {
    getNumber(){
        return 7987
    }
}

full :

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
            }
        },
        methods : {
            getNumber(){
                return 7987
            }
        }
    }
</script>

Now, what if have defined the data in variable above and want to use it in beow method, for that we will use *this* keyword as:

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

**VueJS Events**

1. Create a button in template as:
    *<button type="button">Click me</button>*

2. Apply on click event to the button as:
    *<button v-on:click="test()" type="button">Click me</button>*
    
3. Now create test method in script as:
    methods : {
        test(){
            alert('func running successfully!')
        }
    }

4. Now, we will make a variable named *count* in script using data attribute as:
    data(){
        return {
            count : 0,
        }
    },

5. And, further we will just use the count variable in our view section i.e. 'template' as:
    *<h2>Current Count is : {{ count }}</h2>*

6. Now,to update the value of count variable and display it dynamically on our view, we will update the function test as:
    methods : {
        test(){
            this.count+=1;
        }
    }

7. And, hence we made the function to update the value of count variable on click of the button function.

8. Also, we can apply some more event listeners as:
    *v-on:dblclick* or *@:dblclick* also,
    *v-on:mousemove* or *@:mousemove* etc.


**Two way binding of form inputs in VUE.**

=> In Vue JS, it is very simple to apply two way binding in input fields, just we have to use a attribute named *v-model* with the variable name where we want to store the data after binding, and two way binding is completed.

**Getting the value of input feild**

**Getting the values of checkboxes and radio-buttons**

*for in label is used to select the checkbox or radio-button id it is assigned to.So, that even on the click on the label the respected checkbox or radio-button is selected.*

**Conditional statements in Vue (If/Else)**

To apply the conditional statements in Vue, we need to simply add the attribute to the div or html element as: *v-if="condition"* and *v-else* i.e. : 

    <h2 v-if="show">show</h2>
    <h2 v-else>dont show</h2>

Also, don forget to make the variable in script tag as:
     export default {
        name : 'HelloComponent',
        data(){
            return {
                show : true
            }
        }
    }

*Now, just change the value of show manually and see the changes.*

**For loop in VueJS**

Following is the syntax to be applied to html element as an attribute :

*v-for="**variable** in **dataset**" :key="**unique identifier as key**"*


    