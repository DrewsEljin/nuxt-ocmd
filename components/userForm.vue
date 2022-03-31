<template>
  <section>
    <v-container>
      <form @submit.prevent="storeUser">
        <label for="firstName">First name</label>
        <input id="firstName" v-model="firstname" type="text">
        <label for="lastName">Last name</label>
        <input id="lastName" v-model="lastname" type="text">
        <label for="email">Email</label>
        <input id="email" v-model="mail" type="email">
        <button type="submit">
          Add
        </button>
      </form>
      <div class="users">
        <table>
          <tr>
            <td>Id</td>
            <td>First name</td>
            <td>Last name</td>
            <td>E-mail</td>
          </tr>
          <tr v-for="(user, index) in users" :key="index">
            <td>{{ index }}</td>
            <td>{{ user.firstName }}</td>
            <td>{{ user.lastName }}</td>
            <td>{{ user.email }}</td>
          </tr>
        </table>
      </div>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'UserFormComponent',
  data () {
    return {
      users: []
    }
  },
  mounted () {
    if (localStorage.data) {
      this.users = JSON.parse(localStorage.data)
    }
  },
  methods: {
    storeUser () {
      this.users.push({
        firstName: this.firstname,
        lastName: this.lastname,
        email: this.mail
      })
      this.firstname = ''
      this.lastname = ''
      this.mail = ''
      localStorage.data = JSON.stringify(this.users)
    }
  }
}
</script>

<style scoped>
form {
  font-family: "Roboto";
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
input {
  border: 1px solid #bf8876;
  border-radius: 5px;
  padding: 10px 5px;
}

label {
  margin-top: 20px;
}

button[type="submit"] {
  color: #fff;
  background-color: #46ae46;
  padding: 10px 20px;
  border-radius: 10px;
  font-size: 20px;
  margin-top: 20px;
}

.users {
  margin-top: 20px;
}

.user {
  font-family: "Roboto";
  display: flex;
}

table {
  margin: 0 auto;
  border-collapse: collapse;
  border: 1px solid #000;
}

table tr td {
  padding: 10px 20px;
  font-family: "Roboto";
  border: 1px solid #000;
}

.table-header {
  display: flex;
  font-family: "Roboto";
}
</style>
