<template>
    <div class="ml-10 flex items-baseline">
        <a href="#" class="px-3 py-2 rounded-md text-sm font-medium text-white bg-gray-900 focus:outline-none focus:text-white focus:bg-gray-700">Ver jogos de hoje</a>
        <a 
            v-show="$vuetify.breakpoint.md || $vuetify.breakpoint.lg || $vuetify.breakpoint.xl" 
            href="#" class="ml-4 px-3 py-2 rounded-md text-sm font-medium text-gray-300 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">Ligas Principais</a>
        <a 
            v-show="$vuetify.breakpoint.md || $vuetify.breakpoint.lg || $vuetify.breakpoint.xl"
            href="#" class="ml-4 px-3 py-2 rounded-md text-sm font-medium text-gray-300 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">Outras Ligas</a>
    </div>
</template>