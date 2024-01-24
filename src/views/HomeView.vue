<template>
  <div>
    <!-- Hero Section -->
    <section
      class="bg-gray-500 text-white py-20 transition-all duration-500 ease-in-out"
    >
      <div class="container mx-auto text-center">
        <h1
          class="text-4xl font-bold mb-4 opacity-0 transform translate-y-8 transition-all duration-500 ease-in-out delay-300"
        >
          Welcome to My Website
        </h1>
        <p
          class="text-lg opacity-0 transform translate-y-8 transition-all duration-500 ease-in-out delay-600"
        >
        </p>
        <router-link
          to="/about"
          class="mt-6 inline-block bg-white text-blue-500 py-2 px-4 rounded-full opacity-0 transform translate-y-8 transition-all duration-500 ease-in-out delay-900"
        >
          Learn More
        </router-link>
      </div>
    </section>

    <!-- Features Section -->
    <section class="py-16 transition-all duration-500 ease-in-out delay-1200">
      <div class="container mx-auto">
        <h2
          class="text-3xl font-bold mb-8 text-center opacity-0 transform translate-y-8 transition-all duration-500 ease-in-out delay-1500"
        >
          Key Features
        </h2>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          <!-- Feature Card 1 -->
          <div
            class="bg-white rounded-lg p-6 shadow-md opacity-0 transform translate-y-8 transition-all duration-500 ease-in-out delay-1800"
          >
            <h3 class="text-xl font-bold mb-4">Responsive Design</h3>
            <p>
              Our website is built with a responsive design to provide a
              seamless experience on all devices.
            </p>
          </div>

          <!-- Feature Card 2 -->
          <div
            class="bg-white rounded-lg p-6 shadow-md opacity-0 transform translate-y-8 transition-all duration-500 ease-in-out delay-2100"
          >
            <h3 class="text-xl font-bold mb-4">Vue.js Integration</h3>
            <p>
              We leverage the power of Vue.js to create dynamic and interactive
              user interfaces.
            </p>
          </div>

          <!-- Feature Card 3 -->
          <div
            class="bg-white rounded-lg p-6 shadow-md opacity-0 transform translate-y-8 transition-all duration-500 ease-in-out delay-2400"
          >
            <h3 class="text-xl font-bold mb-4">Tailwind CSS Styling</h3>
            <p>
              Enjoy a beautiful and clean design using Tailwind CSS utility
              classes.
            </p>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "Home",
  mounted() {
    // Add an event listener to trigger animations when the component is mounted
    this.animateOnMount();
  },
  methods: {
    animateOnMount() {
      // Use setTimeout to apply opacity and translation animation after a delay
      setTimeout(() => {
        // Hero Section
        document.querySelector(".bg-gray-500").classList.add("opacity-100");
        document
          .querySelector(".bg-gray-500 h1")
          .classList.add("opacity-100", "translate-y-0");
        document
          .querySelector(".bg-gray-500 p")
          .classList.add("opacity-100", "translate-y-0");
        document
          .querySelector(".bg-gray-500 a")
          .classList.add("opacity-100", "translate-y-0");

        // Features Section
        document.querySelector(".py-16").classList.add("opacity-100");
        document
          .querySelector(".py-16 h2")
          .classList.add("opacity-100", "translate-y-0");

        // Feature Cards
        const featureCards = document.querySelectorAll(".bg-white");
        featureCards.forEach((card, index) => {
          setTimeout(() => {
            card.classList.add("opacity-100", "translate-y-0");
          }, 500 * (index + 1)); // Delay each card animation
        });
      }, 1000); // Initial delay before starting animations
    },
  },
};
</script>

<style scoped>
/* Additional styling if needed */
</style>
