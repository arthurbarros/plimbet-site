<template>
    <nav class="bg-indigo-900">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-24">
                <div class="flex items-center">
                    <div class="flex-shrink-0">
                        <img class="h-16 w-20" src="/PLIMBET-COLORIDA.png">
                    </div>
                    <Baseline/>
                </div>
                
                <ProfileDropdown/>

                <div class="-mr-2 flex md:hidden">
                    <!-- Mobile menu button -->
                    <button @click="toggle"
                        class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-white hover:bg-blue-700 focus:outline-none focus:bg-blue-700 focus:text-white">
                        <svg :class="[isOpen ? 'hidden' : 'block', 'h-6 w-6']" stroke="currentColor" fill="none"
                            viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M4 6h16M4 12h16M4 18h16"></path>
                        </svg>
                        <svg :class="[isOpen ? 'block' : 'hidden', 'h-6 w-6']" stroke="currentColor" fill="none"
                            viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12">
                            </path>
                        </svg>
                    </button>
                </div>
            </div>
        </div>
        <div :class="[isOpen ? '' : 'hidden', 'md:hidden']">
            <div class="px-2 pt-2 pb-3 sm:px-3">
                <link-mobile :href="'#'" :title="'Ligas principais'" :selected="true"/>
                <link-mobile :href="'#'" :title="'Outras principais'" :selected="false"/>

            </div>
            <div class="pt-4 pb-3 border-t border-white">
                <div class="flex items-center px-5">
                    <div class="flex-shrink-0">
                        <img class="h-10 w-10 rounded-full" src="/user.jpg">
                    </div>
                    <div class="ml-3">
                        <div class="text-base font-medium leading-none text-white">Arthur</div>
                        <div class="mt-1 text-sm font-medium leading-none text-gray-400">arthur@email.com</div>
                    </div>
                </div>
                <div class="mt-3 px-2">
                    <a href="#"
                        class="block px-3 py-2 rounded-md text-base font-medium text-gray-400 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">
                        Meus Dados
                    </a>
                    <a href="#"
                        class="mt-1 block px-3 py-2 rounded-md text-base font-medium text-gray-400 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">
                        Historico de apostas    
                    </a>
                    <a href="#"
                        class="mt-1 block px-3 py-2 rounded-md text-base font-medium text-gray-400 hover:text-white hover:bg-gray-700 focus:outline-none focus:text-white focus:bg-gray-700">
                        Sair
                    </a>
                </div>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false
    }
  },
  methods: {
    toggle () {
      this.isOpen = !this.isOpen
    }
  }
}
</script>