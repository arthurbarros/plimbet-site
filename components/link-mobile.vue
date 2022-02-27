<template>      
    <a 
        v-bind:href="href" 
        v-bind:class="[selected ? 'block px-3 py-2 rounded-md text-base font-medium text-white bg-gray-900 focus:outline-none focus:text-white focus:bg-gray-700' : 'mt-1 block px-3 py-2 rounded-md text-base font-medium text-gray-300 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700']">
        {{ title }}
    </a>           
</template>

<script>
  export default {
    props: ['title', 'href', 'selected'],
  }
</script>
