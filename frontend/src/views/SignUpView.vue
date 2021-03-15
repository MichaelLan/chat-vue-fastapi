<template>
  <div class="flex h-screen justify-center items-center">
    <SignUpComponent></SignUpComponent>

  </div>
</template>

<script>
  import SignUpComponent from "@/components/login/SignUpComponent";

  export default {
    name: "SignUpView",
    components: {
      SignUpComponent
    },

  }
</script>

<style scoped>

</style>