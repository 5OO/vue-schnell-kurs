<template>

<!--<pre>{{this.user}}</pre>-->

<div class="container">
  <div class="row">
    <div class="col-md-3">
      <div class="card shadow-lg">
        <div class="card-header bg-success text-white">
          <p class="h3">REgister here </p>
        </div>
        <div class="card-body bg-light">
          <form @submit.prevent="register()">
            <div class="mb-2">
              <input v-model="user.name" class="form-control" placeholder="Name" type="text">
<!--              /* vmodel seob vormi ja state -i  ja meetodid */-->
            </div>
            <div class="mb-2">
              <input v-model="user.email" class="form-control" placeholder="email" type="email">
            </div>
            <div class="mb-2">
              <input v-model="user.password" class="form-control" placeholder="password" type="password">
            </div>
            <div class="mb-2">
              <input class="btn btn-success" type="submit" value="Register">
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Register",
  data: function () {
    return{
      user:{
        name: '',
        email: '',
        password: ''
      }
    };
  },
  methods: {
    register:function () {
      console.log(this.user);
    }
  }
};
</script>

<style scoped>

</style>