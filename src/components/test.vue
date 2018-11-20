<template>
    <div class="test">
        <h1>{{ greeting }}, {{ user.firstName }}</h1>
        
        <p v-if="user.position">
            {{ user.position }}
        </p>
        <input type="text" placeholder="Mad" v-model="thoughts">
        <p><b>What I am thinking:</b> {{ thoughts }}</p>
        <ul class="hobbies">
            <li v-bind:key="item" v-for="item in items">{{item.title}}</li>
        </ul>
        <button v-on:click="greet('Hi, Bud')">Click Me</button>
<input type="text" v-on:keyup="pressKey" v-on:keyup.enter="enterHit">
<hr>
<input type="text" v-model="user.firstName" placeholder="First Name">
<input type="text" v-model="user.lastName" v-on:keyup.enter="enterHit" placeholder="Last Name">

<h3>{{ fullname }}</h3>
    </div>
</template>

<script>
    export default {
        name: 'test',
        data() {
            return {
                greeting: 'Hello',
                thoughts: 'Happy',
                user: {
                    firstName: 'Christopher',
                    lastName: 'Jones',
                    position: 'Graphic Designer'
                },
                showName: true,
                items: [
                    {title: 'Football'},
                    {title: 'Coding'},
                    {title: 'Xbox'},
                    {title: 'Binging' }
                ]
            }
        },
        methods: {
            greet: function(greeting) {
                alert(greeting);
            },
            pressKey: function(e) {
                console.log(e.target.value); 
            },
            enterHit: function() {
                console.log('You hit enter.');
            }
        },
        computed: {
            fullname: function() {
                return this.user.firstName+ ' ' +this.user.lastName;
            }
        }
    }
 </script>

 <style scoped>
    ul.hobbies {
        list-style: none;
    }
    .hobbies li {
        width: 23%;
        padding: 10px 1%;
        background: orange;
        display: inline-block;
        margin: 0;
    }
 </style>