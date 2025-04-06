<script setup>
import Video from './icons/video.vue';
</script>
<template>
    <!-- Banner -->
    <div class="bg-gradient-to-r from-purple-200 to-purple-100 m-4 p-4 rounded-xl flex justify-between items-center shadow">
        <div>
          <p class="text-yellow-700 font-semibold">Did You Miss Any Lecture?</p>
          <h2 class="text-lg font-bold text-purple-800">The Lecture Was Recorded!</h2>
          <button class="bg-yellow-400 px-4 py-1 rounded-full mt-2"><span class="material-icons text-purple-600 reduce">storefront</span>Watch Videos</button>
        </div>

        <Video />
        <!-- <img src="https://placehold.co/120x100?text=Luxury+Trip" class="rounded-xl shadow" alt="Luxury Trip"/> -->
      </div>
      
      <br>
</template>
<style>
  .reduce{
    font-size: inherit !important;
  }
</style>