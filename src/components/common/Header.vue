<template>
  <header class="bg-indigo-600">
    <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8" aria-label="Top">
      <div class="w-full py-6 flex items-center justify-between border-b border-indigo-500 lg:border-none">
        <div class="flex items-center">
          <a href="#">
            <img class="h-10 w-auto" src="https://tailwindui.com/img/logos/workflow-mark.svg?color=white" alt="">
          </a>
          <div class="hidden ml-10 space-x-8 lg:block">
            <router-link :to="{ name: 'Home' }" class="text-base font-medium text-white hover:text-indigo-50">
              Home
            </router-link>
            <router-link :to="{ name: 'Launches' }" class="text-base font-medium text-white hover:text-indigo-50">
              Recent Launches
            </router-link>
            <router-link :to="{ name: 'Missions' }" class="text-base font-medium text-white hover:text-indigo-50">
              Missions
            </router-link>
            <router-link :to="{ name: 'Ships' }" class="text-base font-medium text-white hover:text-indigo-50">
              Ships
            </router-link>
            <router-link :to="{ name: 'Payloads' }" class="text-base font-medium text-white hover:text-indigo-50">
              Payloads
            </router-link>
            <router-link :to="{ name: 'Capsules' }" class="text-base font-medium text-white hover:text-indigo-50">
              Capsules
            </router-link>
            <router-link :to="{ name: 'Dragons' }" class="text-base font-medium text-white hover:text-indigo-50">
              Dragons
            </router-link>
          </div>
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 cursor-pointer mx-3 md:invisible" fill="white" viewBox="0 0 24 24" stroke="white" @click.prevent="isDropDownVisible = !isDropDownVisible">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 5v.01M12 12v.01M12 19v.01M12 6a1 1 0 110-2 1 1 0 010 2zm0 7a1 1 0 110-2 1 1 0 010 2zm0 7a1 1 0 110-2 1 1 0 010 2z" />
          </svg>
        </div>
      </div>
    </nav>
    <transition
      enter-active-class="transition ease-out duration-100"
      enter-class="transform opacity-0 scale-95"
      enter-to-class="transform opacity-100 scale-100"
      leave-active-class="transition ease-in duration-75"
      leave-class="transform opacity-100 scale-100"
      leave-to-class="transform opacity-0 scale-95"
    >
      <div v-if="isDropDownVisible" class="z-10 w-full rounded-md flex flex-col absolute bg-red-300 block text-center px-3 py-4 shadow-lg" aria-orientation="vertical" aria-labelledby="actions-menu">
        <router-link :to="{ name: 'Home' }" class="text-base font-medium text-white hover:text-indigo-50">
          Home
        </router-link>
        <router-link :to="{ name: 'Launches' }" class="text-base font-medium text-white hover:text-indigo-50">
          Recent Launches
        </router-link>
        <router-link :to="{ name: 'Missions' }" class="text-base font-medium text-white hover:text-indigo-50">
          Missions
        </router-link>
        <router-link :to="{ name: 'Ships' }" class="text-base font-medium text-white hover:text-indigo-50">
          Ships
        </router-link>
        <router-link :to="{ name: 'Payloads' }" class="text-base font-medium text-white hover:text-indigo-50">
          Payloads
        </router-link>
        <router-link :to="{ name: 'Capsules' }" class="text-base font-medium text-white hover:text-indigo-50">
          Capsules
        </router-link>
        <router-link :to="{ name: 'Dragons' }" class="text-base font-medium text-white hover:text-indigo-50">
          Dragons
        </router-link>
      </div>
    </transition>
  </header>
</template>

<script>
export default {
  name: 'HeaderComponent',
  data() {
    return {
      isDropDownVisible: false,
    };
  },
};
</script>
