<template>
  <section
    class="relative min-h-[700px] lg:min-h-[850px] flex items-center justify-center text-white overflow-hidden pb-12"
  >
    <!-- Background Image -->
    <div class="absolute inset-0 z-0">
      <img
        src="/images/hero-bg.png"
        alt="Beach Background"
        class="w-full h-full object-cover scale-[1.02]"
      />
      <!-- Subtle dark overlay -->
      <div class="absolute inset-0 bg-black/10"></div>
    </div>

    <!-- Hero Content -->
    <div class="relative z-10 w-full max-w-7xl mx-auto px-4 pt-16 text-center">
      <h1
        class="text-5xl md:text-7xl font-bold mb-6 tracking-tight drop-shadow-xl animate-fade-in-up"
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
</template>
