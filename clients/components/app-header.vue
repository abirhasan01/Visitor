<template>
  <header class="bg-white border-b border-gray-100 sticky top-0 z-50">
    <div
      class="max-w-[1280px] mx-auto px-4 sm:px-6 h-16 sm:h-20 flex items-center justify-between gap-4"
    >
      <!-- Logo -->
      <NuxtLink
        to="/"
        @click="scrollToTop"
        class="flex items-center gap-2 shrink-0"
      >
        <img
          src="/logo.svg"
          alt="viatours"
          class="lg:w-[167px] w-[130px] h-[32px]"
        />
      </NuxtLink>

      <!-- Search Bar (Desktop) -->
      <div class="hidden md:flex flex-1 max-w-lg relative group px-4">
        <div
          class="absolute inset-y-0 left-7 flex items-center pointer-events-none"
        >
          <Search
            class="w-5 h-5 text-gray-400 group-focus-within:text-orange-500 transition-colors"
          />
        </div>
        <input
          type="text"
          placeholder="Search destinations or activities"
          class="w-full pl-12 pr-4 py-2.5 bg-gray-50 border border-gray-200 rounded-full focus:outline-none focus:ring-2 focus:ring-orange-500/20 focus:border-orange-500 transition-all text-[15px] placeholder:text-gray-400"
        />
      </div>

      <!-- Navigation & Actions -->
      <div class="flex items-center gap-2 sm:gap-6">
        <!-- Desktop Nav -->
        <nav class="hidden lg:flex items-center gap-6">
          <NuxtLink
            to="/"
            class="text-[15px] font-medium text-gray-700 hover:text-orange-600 transition-colors"
            >Destinations</NuxtLink
          >
          <NuxtLink
            to="/"
            class="text-[15px] font-medium text-gray-700 hover:text-orange-600 transition-colors"
            >Activities</NuxtLink
          >
          <button
            class="flex items-center gap-1 text-[15px] font-medium text-gray-700 hover:text-orange-600 transition-colors"
          >
            USD
          </button>
        </nav>

        <div class="flex items-center gap-2 sm:gap-4">
          <NuxtLink
            to="/"
            class="hidden sm:block text-[15px] font-medium text-gray-700 hover:text-orange-600 transition-colors"
            >Sign up</NuxtLink
          >
          <NuxtLink
            to="/"
            class="bg-[#eb662b] hover:bg-[#d55a24] text-white px-4 sm:px-8 py-1.5 lg:py-2.5 rounded-full text-[15px] font-semibold transition-all shadow-sm"
          >
            Log in
          </NuxtLink>

          <!-- Mobile Menu Toggle -->
          <button
            class="lg:hidden p-2 text-gray-600 hover:text-orange-600 focus:outline-none"
            @click="isMenuOpen = !isMenuOpen"
          >
            <Menu v-if="!isMenuOpen" class="w-7 h-7" />
            <X v-else class="w-7 h-7" />
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile Menu -->
    <transition name="slide">
      <nav
        v-if="isMenuOpen"
        class="lg:hidden bg-white border-t border-gray-100 absolute w-full shadow-lg z-40"
      >
        <div class="px-6 py-6 flex flex-col gap-4">
          <!-- Mobile Search -->
          <div class="relative md:hidden mb-2">
            <div
              class="absolute inset-y-0 left-3 flex items-center pointer-events-none"
            >
              <Search class="w-5 h-5 text-gray-400" />
            </div>
            <input
              type="text"
              placeholder="Search..."
              class="w-full pl-10 pr-4 py-2 bg-gray-50 border border-gray-200 rounded-lg focus:outline-none focus:border-orange-500"
            />
          </div>
          <NuxtLink
            to="/"
            @click="isMenuOpen = false"
            class="text-lg font-medium text-gray-800 py-2 border-b border-gray-50"
            >Destinations</NuxtLink
          >
          <NuxtLink
            to="/"
            @click="isMenuOpen = false"
            class="text-lg font-medium text-gray-800 py-2 border-b border-gray-50"
            >Activities</NuxtLink
          >
          <NuxtLink
            to="/"
            @click="isMenuOpen = false"
            class="text-lg font-medium text-gray-800 py-2 border-b border-gray-50"
            >Sign up</NuxtLink
          >
          <NuxtLink
            to="/"
            @click="isMenuOpen = false"
            class="text-lg font-medium text-orange-600 py-2"
            >Help Center</NuxtLink
          >
        </div>
      </nav>
    </transition>
  </header>
</template>

<script setup>
import { ref } from "vue";
import { Search, Menu, X } from "lucide-vue-next";

const isMenuOpen = ref(false);

const scrollToTop = () => {
  if (process.client) {
    window.scrollTo({ top: 0, behavior: "smooth" });
  }
};
</script>

<style scoped>
.slide-enter-active,
.slide-leave-active {
  transition: all 0.3s ease-out;
}

.slide-enter-from,
.slide-leave-to {
  transform: translateY(-10px);
  opacity: 0;
}
</style>
