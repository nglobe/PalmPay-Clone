<script setup>
  import Cert from './icons/cert.vue';
</script>

<template>
    <!-- Promo Banner -->
    <div class="m-4">
        <div class="bg-purple-700 text-white p-4 rounded-xl shadow flex justify-between items-center">
          
          <!-- <img src="" class="w-20 rounded" alt="Promo Image"> -->
          <div>
            <p class="text-sm font-semibold">Learn A Skill </p>
            <p class="text-xl font-bold">Enroll Into A Certified Skill Program</p>
            <button class="bg-yellow-500 text-black px-3 float-end py-1 rounded-full mt-2">Enroll Now</button>
          </div>
          <Cert />
        </div>
      </div>
</template>