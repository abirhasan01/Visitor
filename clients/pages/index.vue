<template>
  <section
    class="relative min-h-screen flex items-center justify-center text-white overflow-hidden pb-16"
  >
    <!-- Background Image -->
    <div class="absolute inset-0 z-0">
      <img
        src="/images/hero-bg.png"
        alt="Beach Background"
        class="w-full h-full object-cover object-center"
        style="display: block"
      />
      <!-- Subtle dark overlay -->
      <div class="absolute inset-0 bg-black/10"></div>
    </div>

    <!-- Hero Content -->
    <div
      class="relative z-10 w-full max-w-7xl mx-auto px-4 pt-24 sm:pt-28 text-center"
    >
      <h1
        class="text-4xl md:text-7xl font-bold mb-6 tracking-tight drop-shadow-xl animate-fade-in-up"
      >
        Your world of joy
      </h1>
      <p
        class="text-lg md:text-2xl mb-12 font-[400] opacity-95 drop-shadow-lg leading-relaxed"
      >
        From local escapes to far-flung adventures, find what makes you happy
        anytime, anywhere
      </p>

      <!-- Search Bar -->
      <div
        class="max-w-5xl mx-auto bg-white rounded-2xl p-3 shadow-[0_20px_80px_rgba(0,0,0,0.25)] flex flex-col md:flex-row items-center gap-1 backdrop-blur-sm bg-white/95"
      >
        <!-- Where -->
        <div
          class="flex-1 flex items-center px-6 py-4 border-b md:border-b-0 md:border-r border-gray-100 w-full group"
        >
          <div
            class="p-3 bg-gray-50 rounded-2xl mr-4 group-hover:bg-[#EB662D]/10 transition-colors"
          >
            <MapPin
              class="w-6 h-6 text-gray-500 group-hover:text-[#EB662D] transition-colors"
            />
          </div>
          <div class="text-left flex-1">
            <label
              class="block text-[11px] font-bold text-gray-400 uppercase tracking-widest mb-1.5 leading-none"
              >Where</label
            >
            <input
              type="text"
              placeholder="Search destinations"
              class="w-full bg-transparent text-gray-900 placeholder-gray-400 focus:outline-none font-bold text-base border-none p-0 focus:ring-0"
            />
          </div>
        </div>

        <!-- When -->
        <div
          class="flex-1 flex items-center px-6 py-4 border-b md:border-b-0 md:border-r border-gray-100 w-full group cursor-pointer hover:bg-gray-50/50 transition-colors md:rounded-none"
        >
          <div
            class="p-3 bg-gray-50 rounded-2xl mr-4 group-hover:bg-[#EB662D]/10 transition-colors"
          >
            <Calendar
              class="w-6 h-6 text-gray-500 group-hover:text-[#EB662D] transition-colors"
            />
          </div>
          <div class="text-left flex-1">
            <label
              class="block text-[11px] font-bold text-gray-400 uppercase tracking-widest mb-1.5 leading-none"
              >When</label
            >
            <p class="text-gray-900 font-bold text-base truncate">
              February 05 ~ March 14
            </p>
          </div>
        </div>

        <!-- Tour Type -->
        <div
          class="flex-1 flex items-center px-6 py-4 w-full group cursor-pointer hover:bg-gray-50/50 transition-colors md:rounded-none"
        >
          <div
            class="p-3 bg-gray-50 rounded-2xl mr-4 group-hover:bg-[#EB662D]/10 transition-colors"
          >
            <Flag
              class="w-6 h-6 text-gray-500 group-hover:text-[#EB662D] transition-colors"
            />
          </div>
          <div class="text-left flex-1 relative">
            <label
              class="block text-[11px] font-bold text-gray-400 uppercase tracking-widest mb-1.5 leading-none"
              >Tour Type</label
            >
            <select
              class="w-full bg-transparent text-gray-900 focus:outline-none font-bold text-base appearance-none cursor-pointer border-none p-0 focus:ring-0 px-2"
            >
              <option>All tour</option>
              <option>Adventure</option>
              <option>Relaxation</option>
              <option>Cultural</option>
            </select>
          </div>
        </div>

        <!-- Search Button -->
        <button
          class="w-full md:w-auto bg-[#EB662D] hover:bg-[#d45520] text-white px-14 py-5 rounded-2xl font-extrabold text-lg transition-all duration-500 shadow-[0_15px_30px_rgba(235,102,45,0.4)] hover:shadow-[0_20px_40px_rgba(235,102,45,0.5)] active:scale-95 flex items-center justify-center gap-2"
        >
          <span>Search</span>
        </button>
      </div>
    </div>

    <!-- Bottom Wavy Shape -->
    <div class="absolute bottom-[-1px] left-0 w-full z-20 pointer-events-none">
      <img
        src="/images/hero-shape.png"
        alt="Wave Shape"
        class="w-full h-auto object-cover object-bottom translate-y-2 opacity-100"
      />
    </div>
  </section>

  <section class="py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-24">
      <h2 class="text-3xl md:text-4xl font-bold text-[#05073C] mb-16 px-2">
        Why choose Tourz
      </h2>

      <div
        class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 lg:gap-8"
      >
        <!-- Ultimate flexibility -->
        <div class="flex flex-col gap-6 p-2">
          <div class="w-14 h-14 flex items-center justify-center">
            <img
              src="/images/ticket.svg"
              alt="Ultimate flexibility"
              class="w-full h-full object-contain"
            />
          </div>
          <div class="space-y-3">
            <h3 class="text-xl text-[#05073C] tracking-tight">
              Ultimate flexibility
            </h3>
            <p class="text-[#05073C] text-[15px] leading-[28px]">
              You're in control, with free cancellation and payment options to
              satisfy any plan or budget.
            </p>
          </div>
        </div>

        <!-- Memorable experiences -->
        <div class="flex flex-col gap-6 p-2">
          <div class="w-14 h-14 flex items-center justify-center">
            <img
              src="/images/air_balloon.svg"
              alt="Memorable experiences"
              class="w-full h-full object-contain"
            />
          </div>
          <div class="space-y-3">
            <h3 class="text-xl text-[#05073C] tracking-tight">
              Memorable experiences
            </h3>
            <p class="text-[#05073C] text-[15px] leading-[28px]">
              Browse and book tours and activities so incredible, you'll want to
              tell your friends.
            </p>
          </div>
        </div>

        <!-- Quality at our core -->
        <div class="flex flex-col gap-6 p-2">
          <div class="w-14 h-14 flex items-center justify-center">
            <img
              src="/images/diamond.svg"
              alt="Quality at our core"
              class="w-full h-full object-contain"
            />
          </div>
          <div class="space-y-3">
            <h3 class="text-xl text-[#05073C] tracking-tight">
              Quality at our core
            </h3>
            <p class="text-[#05073C] text-[15px] leading-[28px]">
              High-quality standards. Millions of reviews. A tourz company.
            </p>
          </div>
        </div>

        <!-- Award-winning support -->
        <div class="flex flex-col gap-6 p-2">
          <div class="w-14 h-14 flex items-center justify-center">
            <img
              src="/images/medal.svg"
              alt="Award-winning support"
              class="w-full h-full object-contain"
            />
          </div>
          <div class="space-y-3">
            <h3 class="text-xl text-[#05073C] tracking-tight">
              Award-winning support
            </h3>
            <p class="text-[#05073C] text-[15px] leading-[28px]">
              New price? New plan? No problem. We're here to help, 24/7.
            </p>
          </div>
        </div>
      </div>
    </div>

    <!-- Popular Tours Section -->
    <div class="py-24 bg-[#F5F5F7]">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex items-center justify-between mb-12 px-2">
          <h2 class="text-3xl md:text-4xl font-bold text-[#05073C]">
            Find Popular Tours
          </h2>
          <a
            href="#"
            class="text-sm font-medium text-gray-500 hover:text-[#EB662D] transition-colors"
            >See all</a
          >
        </div>

        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
          <div
            v-for="tour in tours"
            :key="tour.id"
            class="bg-white rounded-2xl overflow-hidden shadow-sm cursor-pointer border border-gray-100"
          >
            <!-- Image Container -->
            <div class="relative aspect-[4/3] overflow-hidden">
              <img
                :src="tour.image"
                :alt="tour.title"
                class="w-full h-full object-cover"
              />
              <button
                class="absolute bottom-3 right-3 w-8 h-8 bg-white rounded-full shadow-sm flex items-center justify-center text-gray-400 hover:text-[#EB662D] transition-colors"
              >
                <Heart class="w-4 h-4" />
              </button>
            </div>

            <!-- Content -->
            <div class="p-5 space-y-2">
              <p class="text-[12px] font-medium text-gray-400">
                {{ tour.location }}
              </p>
              <h3
                class="text-[17px] font-[500] text-[#05073C] leading-tight line-clamp-2 min-h-[3rem]"
              >
                {{ tour.title }}
              </h3>

              <div class="flex items-center gap-1.5 pb-2">
                <div class="flex items-center gap-0.5">
                  <Star class="w-3.5 h-3.5 text-[#EB662D] fill-[#EB662D]" />
                </div>
                <span class="text-sm font-[500] text-[#05073C]">{{
                  tour.rating
                }}</span>
                <span class="text-sm text-gray-400">({{ tour.reviews }})</span>
              </div>

              <div
                class="flex items-center justify-between pt-4 border-t border-gray-100"
              >
                <div class="flex items-center gap-1.5 text-gray-500">
                  <span class="text-[13px] font-medium">{{
                    tour.duration
                  }}</span>
                </div>
                <div class="flex items-center gap-1">
                  <p class="text-[13px] text-gray-400">From</p>
                  <p class="text-[16px] font-[500] text-[#05073C]">
                    ${{ tour.price }}
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Trending Destinations -->
    <div class="py-24 bg-white">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="flex items-center justify-between mb-12">
          <h2 class="text-3xl md:text-4xl font-bold text-[#05073C] mb-16 px-2">
            Trending destinations
          </h2>
          <a
            href="#"
            class="text-sm font-medium text-gray-500 hover:text-[#EB662D] transition-colors"
            >See all</a
          >
        </div>

        <div
          class="grid grid-cols-2 sm:grid-cols-4 lg:grid-cols-8 gap-6 md:gap-4"
        >
          <div
            v-for="destination in destinations"
            :key="destination.id"
            class="flex flex-col items-center group cursor-pointer"
          >
            <div
              class="relative w-full aspect-square mb-4 overflow-hidden rounded-full"
            >
              <img
                :src="destination.image"
                :alt="destination.name"
                class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110"
              />
            </div>
            <div class="text-center">
              <h3
                class="text-base font-[500] text-[#05073C] mb-1 leading-tight"
              >
                {{ destination.name }}
              </h3>
              <p class="text-[13px] text-gray-500 font-medium">
                {{ destination.tours }}
              </p>
            </div>
          </div>
        </div>

        <!-- Pagination Dots -->
        <div class="flex justify-center items-center gap-2 mt-12">
          <button class="w-8 h-1.5 bg-[#05073C] rounded-full"></button>
          <button
            class="w-1.5 h-1.5 bg-gray-300 rounded-full hover:bg-gray-400 transition-colors"
          ></button>
          <button
            class="w-1.5 h-1.5 bg-gray-300 rounded-full hover:bg-gray-400 transition-colors"
          ></button>
          <button
            class="w-1.5 h-1.5 bg-gray-300 rounded-full hover:bg-gray-400 transition-colors"
          ></button>
          <button
            class="w-1.5 h-1.5 bg-gray-300 rounded-full hover:bg-gray-400 transition-colors"
          ></button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { MapPin, Calendar, Flag, Star, Clock, Heart } from "lucide-vue-next";
import destinations from "~/public/data/destinations.json";
import tours from "~/public/data/tours.json";
</script>
