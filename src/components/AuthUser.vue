<template>

<!--  <pre>{{this.isLoggedIn}}</pre>-->

  <h2>Authentication User</h2>
  <div class="container">
    <div class="row">
      <div class="col-md-6">
        <div class="card">
          <div class="card-body">
            <div v-if="isLoggedIn">
              <p class="h3 fw-bolder text-success">teretulemast kasutaja</p>
              <p class="fst-italic">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Adipisci architecto
                aspernatur consectetur culpa doloribus excepturi impedit iste minima molestias nesciunt quisquam soluta
                tempora, tempore temporibus vel velit vero voluptas voluptates.</p>
            </div>
            <div v-if="!isLoggedIn">
              <p class="h3 fw-bolder text-danger">täname sind!</p>
              <p class="fst-italic">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Alias amet blanditiis
                deleniti dicta distinctio doloremque ea earum, enim exercitationem expedita explicabo maiores mollitia
                nihil numquam praesentium qui rerum sed sint.</p>
            </div>
            <div>
              <button v-if="!isLoggedIn" class="btn btn-success btn-sm m-1 shadow" @click="login">Login</button>
              <button v-if="isLoggedIn" class="btn btn-danger btn-sm m-1 shadow" @click="logout">LogOut</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AuthUser",
  data: function () {
    return {
      isLoggedIn: false
    };
  },
  methods: {
    login: function () {
      this.isLoggedIn = true;
    },
    logout: function () {
      this.isLoggedIn= false;
    }
  }
}
</script>

<style scoped>

</style>