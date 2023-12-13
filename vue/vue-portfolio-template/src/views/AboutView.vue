<script setup>
import MainLayout from '../components/MainLayout.vue';

// Page Title of Views
const pageTitle = 'About'
</script>

<template>
  <MainLayout :pageTitle="pageTitle">
    <section class="bg-gray-900 text-white py-8">
      <div class="container mx-auto text-center">
        <p class="text-lg mb-4">
          Let's get to know the author a bit more.
        </p>
      </div>
    </section>

    <div class="max-w-full w-full bg-white p-8 rounded-lg shadow-md mx-auto mt-8">
      <h2 class="text-3xl font-bold text-cyan-800 mb-6">About Me</h2>

      <form @submit.prevent="submitForm">
        <div class="mb-4">
          <h3 class="text-lg font-semibold text-gray-800 mb-2">
            I'm Rey Earl Galos, a BSIT student at Cordova National Highschool. I live in Bangbang, Cordova, Cebu. My hobbies include playing online games and watching movies and anime.
          </h3>
        </div>
      </form>
    </div>
  </MainLayout>
</template>
