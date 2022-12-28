<template>
  <div>
    <div class="logo">
      <img src="./logo_sendx.png" alt="Gumroad logo" />
    </div>
    <button class="left-button">Login With Facebook</button>
  <button class="right-button">Login With Twitter</button>



    <form>
      <label for="email">Email</label>
      <input v-model="email" type="email" id="email" required />
      <br />
      <label for="password">Password</label>
      <input v-model="password" type="password" id="password" required />
      <br />
      <button @click.prevent="login">Log In</button>
      <a href="#" class="forgot-password">Forgot your password?</a>
    </form>
  </div>
</template>

<script>



export default {
  data() {
    return {
      email: "",
      password: "",
    };
  },
  methods: {
    login() {
      // Send a request to the server to log in with the provided email and password
    },
  },
};
</script>

<style>
.left-button {
  margin-right: 10px;
}

.right-button {
  margin-left: 10px;
}


.logo {
  text-align: left;
  margin-bottom: 2rem;
}

.logo img {
  width: 200px;
}

form {
  display: flex;
  flex-direction: column;
}

label {
  margin-bottom: 1rem;
}

input {
  border: 1px solid #ccc;
  border-radius: 4px;
  padding: 1rem;
  margin-bottom: 1rem;
}

button {
  background-color: #0070f3;
  color: white;
  border: none;
  border-radius: 4px;
  padding: 1rem 2rem;
  cursor: pointer;
}

.forgot-password {
  color: #0070f3;
  text-decoration: none;
  margin-top: 1rem;
  display: inline-block;
}
</style>