<template>
    <div class="users">
        <h1>Users</h1>
        <form v-on:submit="addUser">
            <input type="text" v-model="newUser.name" placeholder="Enter name">
            <input type="text" v-model="newUser.email" placeholder="Enter email">
            <input type="submit" value="Submit">
        </form>
        <ul>
            <li v-for="user in users"> 
                <input type="checkbox" class="toggle" v-model="user.contacted">
                <span :class="{contacted: user.contacted}">
                {{ user.name }}: {{user.email}}
                <button v-on:click="deleteUser(user)">x</button>
                </span>
            </li>
            
        </ul>

    </div>
</template>

<script>
    export default {
        name: 'users',
        data() {
            return {
                newUser: {},
                users: [
                    {
                        name: 'Christopher Jones',
                        contacted: false,
                        email: 'thekirkconcept@gmail.com'
                    },
                    {
                        name: 'Steve Smith',
                        contacted: false,
                        email: 'steve@ss.com'
                    },
                    {
                        name: 'Larry Bird',
                        contacted: true,
                        email: 'larry@celtics.com'
                    }
                ]
            }
        },
        methods: {
            addUser: function(e) {
                this.users.push({
                    name: this.newUser.name,
                    email: this.newUser.email,
                    contacted: false
                });
                e.preventDefault();
            },
            deleteUser: function(user) {
                this.users.splice(this.users.indexOf(user), 1);
            }
        },
        created: function() {
            this.$http.get('https://jsonplaceholder.typicode.com/users')
            .then(function(response) {
                console.log(response.data);
            })
        }
    }
 </script>

 <style scoped>
 ul .contacted {
     display:none;
 }
   
 </style>