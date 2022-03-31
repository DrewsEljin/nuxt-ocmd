<template>
  <section>
    <v-container>
      <form @submit.prevent="storeUser">
        <label for="firstName">First name</label>
        <input id="firstName" v-model="firstname" type="text">
        <label for="lastName">Last name</label>
        <input id="lastName" v-model="lastname" type="text">
        <label for="email">Email</label>
        <input id="email" type="email">
        <button type="submit">
          Add
        </button>
      </form>
      <div class="users">
        <div v-for="(user, index) in users" :key="index" class="user">
          <div class="first-name">
            {{ user.firstName }}
          </div>
          <div class="last-name">
            {{ user.lastName }}
          </div>
          <div class="email" />
        </div>
      </div>
    </v-container>
  </section>
</template>

<script>
export default {x
  name: 'UserFormComponent',
  data () {
    return {
      users: [
        { firstName: 'Andrey', lastName: 'Manernyi', email: 'abc@mail.com' }
      ]
    }
  },
  methods: {
    storeUser () {
      this.users.push({ firstName: this.firstname, lastName: this.lastname })
      this.firstname = ''
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

.user {
  font-family: "Roboto";
  display: flex;
}
</style>
