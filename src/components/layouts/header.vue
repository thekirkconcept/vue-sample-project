<template>
    <div class="header">
        <div class="main">
            <div class="logo">
                <h1>Logo</h1>
            </div>
            <div class="navigation">
                <ul>
                    <li class="nav-item" v-for="page in pages">{{ page.name }}</li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>

    export default {
        name: 'header',
        data() {
            return {
                title: 'New Page',
                pages: [
                    {
                        name: 'Home',
                        link: 'home.vue'
                    },
                    {
                        name: 'About',
                        link: 'about.vue'
                    },
                    {
                        name: 'Work',
                        link: 'work.vue'
                    },
                    {
                        name: 'Contact',
                        link: 'contact.vue'
                    }
                ]
            }
        }
        
    }
 </script>

 <style scoped>
 .header {
     width: 100%;
     background: orange;
     display: inline-block;
 }
 .logo {
     float: left;
     width: 20%;
     margin: 0;
     background: red;
 }
 .navigation {
     height: 87px;
     width: 80%;
     background: blue;
     float: left;
 }
.navigation ul {
    list-style: none;
    float: right;
}
.navigation li {
    display: inline-block;
    padding: 5px 30px;
}
    
 </style>