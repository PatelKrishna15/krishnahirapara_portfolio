<template>
  <div class="container bg-gray-500 mx-auto pt-8 pb-8 my-8">
    <h2 class="text-4xl font-bold mb-4 text-center">Contact Us</h2>

    <form @submit.prevent="submitForm" class="max-w-md mx-auto">
      <div class="mb-4 container">
        <label for="name" class="block text-sm font-medium text-gray-600">
          Name
        </label>
        <input
          type="text"
          id="name"
          v-model="formData.name"
          placeholder="Your Name"
          class="mt-1 p-2 w-full border rounded-md focus:outline-none focus:ring focus:border-blue-300"
          required
        />
      </div>

      <div class="mb-4">
        <label for="email" class="block text-sm font-medium text-gray-600">
          Email
        </label>
        <input
          type="email"
          id="email"
          v-model="formData.email"
          placeholder="Your Email"
          class="mt-1 p-2 w-full border rounded-md focus:outline-none focus:ring focus:border-blue-300"
          required
        />
      </div>

      <div class="mb-4">
        <label for="message" class="block text-sm font-medium text-gray-600">
          Message
        </label>
        <textarea
          id="message"
          v-model="formData.message"
          rows="4"
          placeholder="Your Message"
          class="mt-1 p-2 w-full border rounded-md focus:outline-none focus:ring focus:border-blue-300"
          required
        ></textarea>
      </div>

      <button
        type="submit"
        class="bg-blue-500 text-white py-2 px-4 rounded-md hover:bg-blue-600 focus:outline-none focus:ring focus:border-blue-300"
      >
        Submit
      </button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        name: "",
        email: "",
        message: "",
      },
    };
  },
  methods: {
    submitForm() {
      // Send form data to backend server
      fetch("/api/contact", {
        method: "POST",
        headers: {
          "Content-Type": "application/json",
        },
        body: JSON.stringify(this.formData),
      })
        .then((response) => {
          if (response.ok) {
            alert("Message sent successfully!");
            // Reset form fields
            this.formData.name = "";
            this.formData.email = "";
            this.formData.message = "";
          } else {
            alert("Error sending message. Please try again later.");
          }
        })
        .catch((error) => {
          console.error("Error:", error);
          alert("Error sending message. Please try again later.");
        });
    },
  },
};
</script>

<style scoped>
/* Add your custom styles here */
</style>
