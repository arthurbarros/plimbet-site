<template>
    <div class="hidden md:block">
        <div class="ml-4 flex items-center md:ml-6">
            <div class="ml-3 relative">
                <div>
                    <button @click="toggle"
                        class="max-w-xs flex items-center text-sm rounded-full text-white focus:outline-none focus:shadow-solid"
                        id="user-menu" aria-label="User menu" aria-haspopup="true">
                        <img class="h-8 w-8 rounded-full" src="/user.jpg">
                    </button>
                </div>
                <transition enter-active-class="transition ease-out duration-100" enter-class="transform opacity-0 scale-95"
                    enter-to-class="transform opacity-100 scale-100" leave-active-class="transition ease-in duration-75"
                    leave-class="transform opacity-100 scale-100" leave-to-class="transform opacity-0 scale-95">
                    <div v-show="isOpen" class="origin-top-right absolute right-0 mt-2 w-48 rounded-md shadow-lg">
                        <div class="py-1 rounded-md bg-white shadow-xs" role="menu" aria-orientation="vertical"
                            aria-labelledby="user-menu">
                            <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100" role="menuitem">Meus
                                Dados</a>
                            <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100"
                                role="menuitem">Historico de apostas</a>
                            <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100"
                                role="menuitem">Sair</a>
                        </div>
                    </div>
                </transition>
            </div>
        </div>
    </div>
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