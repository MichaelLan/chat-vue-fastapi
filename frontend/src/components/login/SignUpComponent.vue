<template>
  <form class="w-full md:w-80"
        action="" @submit.prevent="onSubmit">
    <div class="flex flex-wrap flex-col w-full">
      <div class="font-bold text-6xl no-underline text-center mb-14 text-green-500">Chat ML</div>
      <div class="text-xs text-left ml-3 text-green-300">Please verify your username or password</div>

      <div class="mx-2">
        <InputPrincipal placeholder="Email" type="text">
          <template v-slot:father-icon-svg>
            <svg :class="classes"
                 xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M16 12a4 4 0 10-8 0 4 4 0 008 0zm0 0v1.5a2.5 2.5 0 005 0V12a9 9 0 10-9 9m4.5-1.206a8.959 8.959 0 01-4.5 1.207"/>
            </svg>
          </template>
        </InputPrincipal>
      </div>

      <div class="mx-2">
        <InputPrincipal placeholder="Username" type="text">
          <template v-slot:father-icon-svg>
            <svg :class="classes"
                 xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"/>
            </svg>
          </template>
        </InputPrincipal>
      </div>


      <div class="mx-2">
        <InputPrincipal placeholder="Password" type="password">
          <template v-slot:father-icon-svg>
            <svg :class="classes"
                 xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M15 7a2 2 0 012 2m4 0a6 6 0 01-7.743 5.743L11 17H9v2H7v2H4a1 1 0 01-1-1v-2.586a1 1 0 01.293-.707l5.964-5.964A6 6 0 1121 9z"/>
            </svg>
          </template>
        </InputPrincipal>
      </div>

      <div class="mx-2">
        <InputPrincipal placeholder="Repeat Password" type="password">
          <template v-slot:father-icon-svg>
            <svg :class="classes"
                 xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                    d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"/>
            </svg>
          </template>
        </InputPrincipal>
      </div>


      <div class="flex flex-col justify-center items-center">
        <ButtonPrincipal type="submit">
          <template #text-button>Sign Up</template>
        </ButtonPrincipal>

        <span class="block text-gray-700">
        Do you a member, <router-link to="/login" class="font-bold hover:text-green-600"> Login! </router-link>
      </span>
      </div>

    </div>
  </form>
</template>

<script>
  import InputPrincipal from "@/components/login/InputPrincipal";
  import ButtonPrincipal from "@/components/login/ButtonPrincipal";

  export default {
    name: "SignUpComponent",
    components: {
      InputPrincipal, ButtonPrincipal
    },
    data() {
      return {
        classes: 'h-4 w-4 text-green-600',
      }
    },
    methods: {
      onSubmit(){
        console.log("Estoy desde el sign up")
      },
    }
  }
</script>

<style scoped>

</style>