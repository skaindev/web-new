<template>
  <div class="min-h-screen flex flex-col bg-black text-white">
    <!-- HERO SECTION -->
    <section class="relative h-screen w-full overflow-hidden flex items-center justify-center">
      <img
        src="/assets/background.png"
        alt="background"
        class="absolute inset-0 w-full h-full object-cover opacity-60"
      />

      <div class="relative z-10 text-center p-8 max-w-4xl mx-auto">
        <img
          src="/assets/logo.png"
          alt="logo"
          class="mx-auto w-40 h-40 mb-6"
        />
        <h1 class="text-5xl font-bold mb-4 tracking-wide">Skaina Project</h1>
        <p class="text-lg opacity-80 max-w-2xl mx-auto">
          A futuristic blockchain ecosystem bridging finance, creativity, and scalability.
        </p>

        <button class="mt-8 px-8 py-3 bg-purple-600 hover:bg-purple-700 rounded-full text-lg font-semibold transition-all">
          Explore More
        </button>
      </div>
    </section>

    <!-- FEATURES SECTION -->
    <section class="py-24 bg-gradient-to-b from-black to-purple-900">
      <div class="max-w-6xl mx-auto px-6 grid md:grid-cols-3 gap-12">
        <div class="p-6 bg-purple-800/40 rounded-2xl shadow-lg text-center hover:scale-105 transition-transform">
          <h3 class="text-2xl font-bold mb-4">High Scalability</h3>
          <p class="opacity-75">Next-generation blockchain throughput optimized for global adoption.</p>
        </div>
        <div class="p-6 bg-purple-800/40 rounded-2xl shadow-lg text-center hover:scale-105 transition-transform">
          <h3 class="text-2xl font-bold mb-4">AI Integration</h3>
          <p class="opacity-75">Smart automation and intelligent computation embedded into the network.</p>
        </div>
        <div class="p-6 bg-purple-800/40 rounded-2xl shadow-lg text-center hover:scale-105 transition-transform">
          <h3 class="text-2xl font-bold mb-4">Cross-Chain</h3>
          <p class="opacity-75">Seamless interoperability between major blockchain ecosystems.</p>
        </div>
      </div>
    </section>

    <!-- ABOUT SECTION -->
    <section class="py-32 bg-black">
      <div class="max-w-5xl mx-auto px-6 grid md:grid-cols-2 gap-12 items-center">
        <div>
          <h2 class="text-4xl font-bold mb-6">What Is Skaina?</h2>
          <p class="text-lg opacity-80 leading-relaxed">
            Skaina Project is a futuristic blockchain architecture designed to merge AI,
            creativity, scalability, and real-world utility into one cohesive digital ecosystem.
          </p>
        </div>

        <img
          src="/assets/background.png"
          alt="about graphic"
          class="rounded-2xl shadow-xl opacity-90"
        />
      </div>
    </section>

    <!-- FOOTER -->
    <footer class="py-12 bg-purple-900/30 text-center">
      <p class="opacity-70">© 2025 Skaina Project — All rights reserved.</p>
    </footer>
  </div>
</template>

<script setup>
// Page-level logic if needed
</script>

<style scoped>
/* Example simple animations */
@keyframes float {
  0% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
  100% { transform: translateY(0); }
}
.animate-float {
  animation: float 4s ease-in-out infinite;
}
</style>
