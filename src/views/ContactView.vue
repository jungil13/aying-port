<template>
<section class="py-8 px-4 md:px-20 bg-gray-700 mb-1">
  <div class="max-w-3xl mx-auto">
    <h2 class="text-3xl font-extrabold text-white mb-6 text-center">Contact Me</h2>
    <!-- Contact Form -->
    <form>
      <!-- Name Input -->
      <div class="mb-4">
        <label for="name" class="block text-white mb-2">Name</label>
        <input type="text" id="name" name="name" placeholder="Enter your name" class="w-full px-4 py-2 rounded-lg bg-gray-800 text-white focus:outline-none focus:bg-gray-900">
      </div>
      <!-- Email Input -->
      <div class="mb-4">
        <label for="email" class="block text-white mb-2">Email</label>
        <input type="email" id="email" name="email" placeholder="Enter your email address" class="w-full px-4 py-2 rounded-lg bg-gray-800 text-white focus:outline-none focus:bg-gray-900">
      </div>
      <!-- Message Input -->
      <div class="mb-6">
        <label for="message" class="block text-white mb-2">Message</label>
        <textarea id="message" name="message" rows="5" placeholder="Enter your message" class="w-full px-4 py-2 rounded-lg bg-gray-800 text-white focus:outline-none focus:bg-gray-900"></textarea>
      </div>
      <!-- Submit Button -->
      <button type="submit" class="w-full bg-green-500 text-white py-2 px-4 rounded-lg hover:bg-blue-600 transition duration-200">Send Message</button>
    </form>
  </div>
</section>

</template>
<script>
</script>