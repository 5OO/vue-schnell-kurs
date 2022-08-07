<template>
  <div class="container">
    <div class="grid">
      <div class="row">
        <div class="col">
          <p class="h3">App component</p>
          <p class="fst-italic">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ad aliquam asperiores
            assumenda autem beatae cum delectus dignissimos, doloribus et, inventore iusto laboriosam, laborum nemo
            perferendis perspiciatis repudiandae sapiente tenetur voluptas.</p>

        </div>
      </div>
    </div>

    <user-list/>

  </div>

</template>

<script>

import UserList from "@/components/UserList";

export default {
  components: {UserList}
}
</script>
<style>
@import "styles.css";
</style>
