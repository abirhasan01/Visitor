<template>
  <footer class="bg-[#faf5f0] py-24 text-[#051036]">
    <div class="max-w-[1280px] mx-auto px-6">
      <div
        class="grid grid-cols-2 md:grid-cols-2 lg:grid-cols-4 gap-12 lg:gap-8"
      >
        <!-- Contact Section -->
        <div class="col-span-2 md:col-span-1">
          <h3 class="text-[17px] font-semibold mb-8">Contact</h3>
          <div class="space-y-4">
            <p class="text-[15px] leading-relaxed text-[#051036] opacity-80">
              328 Queensberry Street, North Melbourne VIC3051, Australia.
            </p>
            <p class="text-[15px] font-medium text-[#051036]">
              hi@viatours.com
            </p>
          </div>
        </div>

        <!-- Company Section -->
        <div class="col-span-1">
          <h3 class="text-[17px] font-semibold mb-8">Company</h3>
          <ul class="space-y-4">
            <li v-for="link in companyLinks" :key="link.name">
              <NuxtLink
                :to="link.href"
                class="text-[15px] text-[#051036] opacity-80 hover:opacity-100 transition-opacity"
              >
                {{ link.name }}
              </NuxtLink>
            </li>
          </ul>
        </div>

        <!-- Support Section -->
        <div class="col-span-1">
          <h3 class="text-[17px] font-semibold mb-8">Support</h3>
          <ul class="space-y-4">
            <li v-for="link in supportLinks" :key="link.name">
              <NuxtLink
                :to="link.href"
                class="text-[15px] text-[#051036] opacity-80 hover:opacity-100 transition-opacity"
              >
                {{ link.name }}
              </NuxtLink>
            </li>
          </ul>
        </div>

        <!-- Newsletter & Mobile Apps Section -->
        <div class="col-span-2 md:col-span-1 flex flex-col">
          <!-- Newsletter -->
          <div class="mb-12">
            <h3 class="text-[17px] font-semibold mb-6">Newsletter</h3>
            <p class="text-[15px] text-[#051036] opacity-80 mb-6">
              Subscribe to the free newsletter and stay up to date
            </p>
            <div
              class="flex items-center bg-white rounded-xl border border-gray-100 p-1 w-full max-w-[400px] overflow-hidden"
            >
              <input
                type="email"
                placeholder="Your email address"
                class="min-w-0 flex-grow bg-transparent px-4 py-2 text-[15px] outline-none placeholder:text-gray-400"
              />
              <button
                class="shrink-0 px-6 py-2.5 text-[15px] font-semibold text-[#051036] hover:text-[#3554d1] transition-colors"
              >
                Send
              </button>
            </div>
          </div>

          <!-- Mobile Apps -->
          <div>
            <h3 class="text-[17px] font-semibold mb-6">Mobile Apps</h3>
            <ul class="space-y-4">
              <li>
                <a
                  href="#"
                  class="text-[15px] text-[#051036] opacity-80 hover:opacity-100 transition-opacity"
                >
                  iOS App
                </a>
              </li>
              <li>
                <a
                  href="#"
                  class="text-[15px] text-[#051036] opacity-80 hover:opacity-100 transition-opacity"
                >
                  Android App
                </a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
const companyLinks = [
  { name: "About Us", href: "#" },
  { name: "Tourz Reviews", href: "#" },
  { name: "Contact Us", href: "#" },
  { name: "Travel Guides", href: "#" },
  { name: "Data Policy", href: "#" },
  { name: "Cookie Policy", href: "#" },
  { name: "Legal", href: "#" },
  { name: "Sitemap", href: "#" },
];

const supportLinks = [
  { name: "Get in Touch", href: "#" },
  { name: "Help center", href: "#" },
  { name: "Live chat", href: "#" },
  { name: "How it works", href: "#" },
];
</script>

<style scoped>
footer {
  font-family: "Inter", sans-serif;
}
</style>
