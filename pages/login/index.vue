<template>
  <div class="bg d-flex">
    <div class="row">
      <div class="left col-md-6">
        <div class="container mt-5 text-white">
          <h3>Login</h3>
          <p class="mt-3">
            By logging into Fullstack Academy, you agree to our Terms of use and
            Privacy Policy.
          </p>
        </div>
      </div>
      <div class="col-md-6">
        <div class="container mt-5">
          <form @submit.prevent="userLogin">
            <div class="form-group">
              <label for="email">Email</label>
              <input
                type="email"
                class="form-control mb-2"
                v-model="login.email"
              />
            </div>
            <div class="form-group">
              <label for="password">Password</label>
              <input
                type="password"
                class="form-control"
                v-model="login.password"
              />
            </div>

            <div class="mt-4 ">
              <a href="/">
                Forgot password?
              </a>
              <button
                type="submit"
                class="submit btn btn-primary btn-block"
                style="margin-top:5px"
              >
                Log in
              </button>
              <div class="text-center mt-3">
                <a href="/" class="text-center">Create an account</a>
              </div>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  layout: "login",
  data() {
    return {
      login: {
        username: "",
        password: ""
      }
    };
  },
  methods: {
    async userLogin() {
      try {
        let response = await this.$auth.loginWith("local", {
          data: this.login
        });
        console.log(response);
      } catch (err) {
        console.log(err);
      }
    }
  }
};
</script>

<style scoped>
.bg {
  height: 100vh;
}
.row {
  background-color: rgb(255, 255, 255);
  max-width: 800px;
  height: 100vh;
  margin: auto;
  height: 70vh;
}

.left {
  background-color: #6750c0;
  background-image: linear-gradient(316deg, #7059c9 0%, #7b47b3 74%);
}
</style>
