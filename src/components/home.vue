<template>
    <div class="home-page">
        <Header></Header>
        <Body></Body>
        <Footer></Footer>
    </div>
</template>

<script>
import Header from './layouts/header'
import Body from './layouts/body'
import Footer from './layouts/footer'

    export default {
        name: 'home',
        components: {
            Header, Body, Footer
        },
        data() {
            return {
                
            }
        }
        
    }
 </script>

 <style scoped>
    
 </style>