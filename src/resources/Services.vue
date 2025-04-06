<template>

  
      <!-- Services Area -->
      <div class="m-4 bg-white rounded-lg p-4 shadow">
        <div class="flex justify-between items-center mb-3">
          <h3 class="font-semibold text-lg">Services</h3>
          <button class="text-purple-600 text-sm more">More</button>
        </div>
        <div
          class="overflow-x-auto whitespace-nowrap scrollbar-hide scroll-smooth"
          ref="scrollRef"
          @scroll="onScroll"
        >
          <div class="inline-flex w-full space-x-4">
            <div
              v-for="(page, index) in servicePages"
              :key="index" 
              class="grid grid-cols-4 gap-4 text-center text-sm text-gray-700 min-w-full"
            >
              <div v-for="(item, idx) in page" :key="idx" @click="handleClik(item.name)">

                <span class="material-icons text-purple-600">{{ item.icon }}</span>
                <p>{{ item.name }}</p>
              </div>
            </div>
          </div>
        </div>
  
        <!-- Swipe Indicators -->
        <div class="flex justify-center mt-3 gap-2">
          <span
            v-for="(dot, index) in servicePages.length"
            :key="'dot' + index"
            class="w-2 h-2 rounded-full"
            :class="{
              'bg-purple-600': activePage === index,
              'bg-gray-400': activePage !== index
            }"
          ></span>
        </div>
      </div>
  
     
  <br>
      
    
  </template>
  
  <script>
 
// import {  } from "module";
  export default {
    name: "Services",
    data() {
      return {
        activePage: 0,
        servicePages: [
          [
            { icon: "storefront", name: "Merchant" },
            { icon: "school", name: "WAEC" },
            { icon: "commute", name: "Transport" },
            { icon: "card_giftcard", name: "Gift Card" },
            { icon: "wifi", name: "Internet" },
            { icon: "savings", name: "Savings" },
            { icon: "favorite", name: "Invitation" },
            { icon: "attach_money", name: "Trial Cash" },
            { icon: "menu_book", name: "Education" },
            { icon: "shopping_cart", name: "E-shop" },
            { icon: "verified", name: "JAMB" },
            { icon: "water_drop", name: "Water" }
          ],
          [
            { icon: "flash_on", name: "Electricity" },
            { icon: "payment", name: "Bills" },
            { icon: "smartphone", name: "Airtime" },
            { icon: "subscriptions", name: "TV" },
            { icon: "qr_code", name: "Scan Pay" },
            { icon: "language", name: "Browser" },
            { icon: "verified_user", name: "Verify" },
            { icon: "group", name: "Community" },
            { icon: "apartment", name: "Housing" },
            { icon: "redeem", name: "Rewards" },
            { icon: "local_atm", name: "ATM Nearby" },
            { icon: "support_agent", name: "Support" }
          ]
        ]
//   const handleClik = (name)=>{
//     console.log(name);
//   }

      };
    },
    methods: {
      onScroll() {
        const scrollX = this.$refs.scrollRef.scrollLeft;
        const width = this.$refs.scrollRef.offsetWidth;
        this.activePage = scrollX < width / 2 ? 0 : 1;
      },
      handleClik(name){
        console.log(name);
        
      }
    }
  };
  </script>
  
  <style>
  @import url("https://fonts.googleapis.com/icon?family=Material+Icons");
  
  .scrollbar-hide::-webkit-scrollbar {
    display: none;
  }
  .scrollbar-hide {
    -ms-overflow-style: none;
    scrollbar-width: none;
  }
  </style>