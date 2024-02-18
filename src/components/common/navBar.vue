<template>
  <div class="bg-white">
    <header class="absolute inset-x-0 top-0 z-50">
      <div
        class="flex items-center justify-between p-6 lg:px-8"
        aria-label="Global"
      >
        <!-- Move the menu button to the right -->
        <div class="flex items-center justify-end w-full">
          <span
            class="material-symbols-outlined cursor-pointer"
            @click="toggleMenu"
          >
            menu
          </span>
        </div>
      </div>
      <br />

      <div class="mx-3">
        <nav
          :class="getMenuClass()"
          class="text-center mx-auto lg:w-4/5 xl:w-3/5 opacity-70 border border-gray-300 rounded-md bg-gray-100/70"
        >
          <div class="container-links">
            <ul
              class="list-none grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4 p-1 justify-center"
            >
              <li class="text-center">
                <a
                  href="#"
                  class="nav-link px-1 py-2 hover:bg-yellow-500/50 font-bold tracking-tight text-gray-900"
                  >Cadastro</a
                >
              </li>
              <li class="text-center">
                <a
                  href="#"
                  class="nav-link px-1 py-2 hover:bg-yellow-500/50 font-bold tracking-tight text-gray-900"
                  >Cardápio</a
                >
              </li>
              <li class="text-center">
                <a
                  href="#"
                  class="nav-link px-1 py-2 hover:bg-yellow-500/50 font-bold tracking-tight text-gray-900"
                  >Home</a
                >
              </li>
            </ul>
          </div>
        </nav>
      </div>
    </header>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

const getMenuClass = () => {
  return isMenuOpen.value ? "" : "hidden";
};
</script>
