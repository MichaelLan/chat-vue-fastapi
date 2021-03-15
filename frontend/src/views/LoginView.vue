<template>
  <div class="flex h-screen justify-center items-center">
      <LoginComponent></LoginComponent>
  </div>
</template>

<script>
  import LoginComponent from "@/components/login/LoginComponent";

  export default {
    name: "Login",
    components: {
      LoginComponent,
    }
  }
</script>
