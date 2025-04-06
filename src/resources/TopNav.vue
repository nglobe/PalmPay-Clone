<script setup>
import Funding from './Funding.vue';
</script>
<template>
      <!-- Top Section -->
      <div class="bg-white shadow p-4 flex justify-between items-center top-nav">
        <div class="flex items-center gap-3 top-nav">
          <img src="https://randomuser.me/api/portraits/men/75.jpg" class="w-10 h-10 rounded-full" alt="Profile">
          <div>
            <p class="font-bold">Hi, Nglobers LL</p>
            <p class="text-sm text-gray-500">Welcome, let's make payments!</p>
          </div>
        </div>
        <div class="flex items-center gap-4">
          <span class="material-icons text-purple-600">headphones</span>
          <div class="relative">
            <span class="material-icons text-red-600">notifications</span>
            <span class="absolute -top-1 -right-2 bg-red-600 text-white text-xs px-1 rounded-full">1</span>
          </div>
        </div>
      </div>
      <br>

      <!-- <div class="min-h-screen bg-gray-100 p-4 text-gray-800 font-sans"> -->
    <!-- Top Card -->
    
    <Funding />
    <br>

    
</template>

<style>
  .top-nav{
    margin: 0!important;
  }
</style>