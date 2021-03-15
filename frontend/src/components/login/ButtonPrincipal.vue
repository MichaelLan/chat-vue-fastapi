<template>
  <button :type="type"
     class="block text-center border-4 ring-4 px-10 py-3 rounded-full font-bold bg-green-500 text-white border-white ring-green-100 m-10 focus:outline-none hover:bg-green-600 hover:ring-green-200">
    <slot name="text-button">
      <span>
        Text here
      </span>
    </slot>
  </button>
</template>
<script>
  export default {
    name: 'ButtonPrincipal',
    props: ['type'],
  }
</script>