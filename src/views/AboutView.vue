<template>
  <main class="container bg-gray-500 mx-auto my-8">
    <div class="flex flex-col md:flex-row space-y-4 md:space-y-0 md:space-x-8">
      <!-- Left Content -->
      <div class="md:w-1/2 m-20 mt-26 mb-20">
        <h1 class="text-5xl font-bold mb-20">About Us</h1>
        <h1 class="text-3xl font-size:8rem">Hello There!</h1>
        <p class="text-black-600 ">
          I'm Krishna Hirapara, a Junior Laravel Developer at Alphabit Infoway
          with an interest in software development, PHP Laravel training, and
          front-end development.
        </p>
      </div>

      <!-- Right Content (Image) -->
      <div class="group inline-block">
        <img
          class="w-40 mt-20 h-auto transition-transform transform hover:scale-110 hover:rotate-2 group-hover:bg-blue-500"
          src="@/assets/images.jfif"
          alt="Your Image"
        />
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: "About",
};
</script>

<style scoped>
.group-hover\:filter:hover {
  filter: brightness(150%);
}
/* Additional styling if needed */
</style>
