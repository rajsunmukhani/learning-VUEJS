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

1. vue (syntax highlight for vuejs) *jcbuisson*
2. vue format (a beutify extension for .vue file) *fc_bean*