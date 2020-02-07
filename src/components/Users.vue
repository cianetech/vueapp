<template>
    <div class="container">
        <h3>Users:</h3>
        <table>
            <thead>
                <tr>
                    <th>ID</th>
                    <th>Name</th>
                    <th>Email</th>
                    <th>City</th>
                </tr>

            </thead>
            <tbody></tbody>
        </table>
    </div>
</template>

<script>
import axios from 'axios';

export default {
    name: 'Users',
    data() {
        return {
            users: null
        };
    },
    created: function() {
        axios
            .get('https://jsonplaceholder.typicode.com/users')
            .then(res => {
                this.users = res.data;
            })
    }
}
</script>

<style>
    h3 {
        margin-bottom: 5%;
    }
</style>