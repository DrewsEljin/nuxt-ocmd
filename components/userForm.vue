<template>
  <section>
    <v-container>
      <form @submit.prevent="addUser">
        <label for="firstName">First name *</label>
        <input
          id="firstName"
          v-model="firstname"
          required
          type="text"
          placeholder="First Name"
        >
        <label for="lastName">Last name *</label>
        <input
          id="lastName"
          v-model="lastname"
          required
          type="text"
          placeholder="Last Name"
        >
        <label for="email">Email *</label>
        <input
          id="email"
          v-model="mail"
          required
          type="email"
          placeholder="E-mail"
        >
        <button type="submit">
          Add
        </button>
      </form>
      <div
        class="notification"
        :class="{ active: isError }"
        v-html="errorMessage"
      >
        test
      </div>
      <div class="users">
        <table>
          <tr>
            <td>Id</td>
            <td>First name</td>
            <td>Last name</td>
            <td>E-mail</td>
            <td />
          </tr>
          <tr v-for="(user, index) in users" :key="index">
            <td>{{ index }}</td>
            <td>{{ user.firstName }}</td>
            <td>{{ user.lastName }}</td>
            <td>{{ user.email }}</td>
            <td class="delete" @click="deleteItem(user.id)">
              &times;
            </td>
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
      errorMessage: null,
      isError: null,
      firstname: null,
      lastname: null,
      mail: null,
      users: null
    }
  },
  mounted () {
    if (localStorage.data) {
      this.users = JSON.parse(localStorage.data)
    } else {
      this.users = []
    }
  },
  methods: {
    store () {
      localStorage.data = JSON.stringify(this.users)
    },
    addUser () {
      if (
        this.validateMail(this.mail) === true &&
        this.validateText([this.firstname, this.lastname])
      ) {
        this.users.push({
          firstName: this.firstname,
          lastName: this.lastname,
          email: this.mail,
          id: Date.now()
        })
        this.firstname = ''
        this.lastname = ''
        this.mail = ''
        this.store()
        this.errorValidation('')
        this.isError = false
      }
    },
    validateText (array) {
      for (let element of array) {
        element = element.replace(/\s/g, '')
        if (element.length <= 0 || element.length >= 17) {
          this.errorValidation(
            'First and last name must contain from 1 to 16 letters(spaces does not count)'
          )
          return false
        }
        if (!element.match(/^[a-zA-Z_]+$/)) {
          this.errorValidation('Please enter only letters')
          return false
        }
      }
      return true
    },
    validateMail (mail) {
      for (const element of this.users) {
        if (element.email === mail) {
          this.error = true
          this.errorValidation('This e-mail is already using')
          return false
        }
      }
      return true
    },
    errorValidation (msg) {
      this.isError = true
      this.errorMessage = msg
    },
    deleteItem (id) {
      this.users = this.users.filter(e => e.id !== id)
      this.store()
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
  border: 1px solid #ccc;
  padding: 15px 20px;
}

label {
  margin-top: 20px;
  margin-bottom: 10px;
}

button[type="submit"] {
  color: #fff;
  background-color: #46ae46;
  padding: 10px 20px;
  border-radius: 10px;
  font-size: 20px;
  margin-top: 20px;
  min-width: 10rem;
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

.delete {
  cursor: pointer;
  font-size: 20px;
  background-color: red;
  color: #fff;
}

.notification {
  font-family: "Roboto";
  font-size: 20px;
  padding: 10px 20px;
  background-color: #ffb900;
  margin-top: 20px;
  color: #fff;
  display: none;
}
.notification.active {
  display: block;
}
</style>
