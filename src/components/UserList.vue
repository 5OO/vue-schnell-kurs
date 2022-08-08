<template>
  <!--<h2>User List tuleb siit </h2>-->
  <!--  https://jsonplaceholder.typicode.com/users -->
<!--mt-3 margin top 3-->

  <div class="container mt-3">
    <div class="row">
      <div class="col">
        <p class="h3 fw-bolder text-success">User list</p>
        <p class="fst-italic">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Alias, assumenda at deleniti
          dolorem eaque enim fuga impedit in ipsam labore modi molestiae nesciunt, nostrum recusandae rem sint sunt vel,
          voluptate.</p>
      </div>
      <div v-if="loading">
        <Spinner/>
      </div>
      <div v-if="errorMessage">
        <p class="fw-bold text-danger">{{errorMessage}}</p>
      </div>
      <div v-if="!loading && users.length > 0 " class="row">
        <div class="col">
          <table class="table table-hover text-center table-striped">
            <thead class="bg-success text-white">
            <tr>
              <th>no #</th>
              <th>name</th>
              <th>email</th>
              <th>company</th>
              <th>website</th>
              <th>location</th>
            </tr>
            </thead>
            <tbody>
            <tr v-for=" user in users" :key="user.id">
              <td>{{ user.id }}</td>
              <td>
                <router-link :to="'/users/' + user.id" class="text-decoration-none fw-bold text-success">{{ user.name }}</router-link>
              </td>
              <td>{{ user.email }}</td>
              <td>{{ user.company.name }}</td>
              <td>{{ user.website }}</td>
              <td>{{ user.address.city }}</td>
            </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import {UserService} from "@/services/UserService";

export default {
  name: "UserList",
  components: {},

  data: function () {
    return {
      loading: false,
      users: [],
      errorMessage: null
    };
  },
  created: async function () {
    try {
      this.loading = true;
      let response = await UserService.getAllUsers();
      this.loading = false;
      this.users = response.data;
    } catch (error) {
      this.loading = false;
      this.errorMessage = error;
    }
  }
}
</script>

<style scoped>

</style>