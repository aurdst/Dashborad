<template>
    <div class="container">
      <h1>Liste des utilisateurs</h1>
      <table class="table">
        <thead>
          <tr>
            <th>ID</th>
            <th>Nom</th>
            <th>Identifiant</th>
            <th>Email</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="user in users" :key="user.id">
            <td>{{ user.id }}</td>
            <td>{{ user.name }}</td>
            <td>{{ user.username }}</td>
            <td>{{ user.email }}</td>
          </tr>
        </tbody>
      </table>
    </div>
</template>
  

<script>
    export default {
        name: 'OngletData',
        data() {
            return {
                users: [],
            };
        },
        mounted() {
            this.fetchData();
        },
        methods: {
            fetchData() {
            fetch("https://jsonplaceholder.typicode.com/users")
                .then(response => response.json())
                .then(data => {
                    console.log(data);
                    this.users = data;
                })
                .catch(error => {
                    console.error("ERREUR :", error);
                })
            }
        },
    }
</script>