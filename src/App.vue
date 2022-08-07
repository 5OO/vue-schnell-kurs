<template>
<div class="container">
  <div class="grid">
    <div class="row">
      <div class="col">
        <p class="h3">App component</p>
        <p class="fst-italic">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ad aliquam asperiores assumenda autem beatae cum delectus dignissimos, doloribus et, inventore iusto laboriosam, laborum nemo perferendis perspiciatis repudiandae sapiente tenetur voluptas.</p>

      </div>
    </div>
  </div>

<auth-user/>

</div>

</template>

<script>

import AuthUser from "@/components/AuthUser";
export default {
  components: {AuthUser  }
}
</script>
<style>
@import "styles.css";
</style>
