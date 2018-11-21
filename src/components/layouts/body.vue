<template>
    <div class="body">
        <Content></Content>
    </div>
</template>

<script>
import Content from './content/homepage'
    export default {
        name: 'body',
        components: {
            Content
        },
        data() {
            return {
               
            }
        }
        
    }
 </script>

 <style scoped>
 .body {
     width: 100%;
     clear:both;
     background: yellow;
 }
    
 </style>