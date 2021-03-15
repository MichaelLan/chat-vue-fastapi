<template>
  <div class="relative w-full flex items-center">
    <LabelInput>
      <template v-slot:icon-svg>
        <slot name="father-icon-svg"></slot>
      </template>

    </LabelInput>
    <input :type="type" :placeholder="placeholder"
           class="flex focus:outline-none focus:ring-2 focus:ring-green-500 focus:shadow-lg text-gray-600 rounded-full px-5 pl-14 pr-10 py-3 my-2 border-2 border-gray-200 w-full"/>
  </div>
</template>
<script>
  import LabelInput from "@/components/login/LabelInput"

  export default {
    name: 'InputPrincipal',
    props: ['placeholder', 'type'],
    components: {LabelInput},
    filters: {
      capitalize: function (value) {
        if (!value) return ''
        value = value.toString()
        return value.charAt(0).toUpperCase() + value.slice(1)
      }
    }
  }
</script>