<template>
  <div>
    <header
      class="
        sticky
        top-0
        z-40
        h-16
        w-full
        border-b border-b-indigo-100
        bg-gray-100
        px-3
      "
    >
      <div class="flex h-full w-full items-center justify-between">
        <div class="flex items-center">
          <HomeIcon class="w-8 fill-indigo-500" />
          <span class="font-semibold">Estatery</span>
        </div>
        <div class="lg:hidden">
          <MenuIcon class="w-8 cursor-pointer" @click="MenuOpen = !MenuOpen" />
        </div>
        <nav
          class="
            absolute
            left-0
            top-16
            w-full
            -translate-y-[200%]
            bg-slate-300
            pl-2
            lg:relative lg:top-0 lg:w-fit lg:translate-y-0 lg:bg-transparent
          "
          :class="MenuOpen && 'translate-y-0'"
        >
          <ul class="flex flex-col gap-8 py-4 font-bold lg:flex-row">
            <li>Rent</li>
            <li>Buy</li>
            <li>Sell</li>
            <li>Manage Property</li>
            <li>Ressources</li>
          </ul>
        </nav>
        <div class="menu-text gap-4">
          <button class="bouton2 mt-1 mb-1 font-bold text-[#6366F1]">
            Login
          </button>
          <button class="bouton1 mr-2 mt-1 mb-1 font-bold text-white">
            Sign Up
          </button>
        </div>
      </div>
    </header>
    <main class="bg-gray-50 py-14 px-4 font-inter">
      <div class="mx-auto mb-7 flex w-4/5 flex-col gap-7">
        <div class="flex flex-col gap-7 lg:flex-row lg:justify-between">
          <h2 class="text-center text-4xl font-bold text-indigo-900">
            Search properties to rent
          </h2>
          <div class="flex items-center">
            <input
              type="search"
              placeholder="Search with Search Bar"
              class="
                h-12
                w-full
                rounded-lg
                border-2 border-indigo-100
                px-4
                placeholder:text-xs
              "
            />
            <ChevronDownIcon
              class="
                -ml-8
                h-5
                w-5
                rounded-full
                bg-indigo-100
                stroke-indigo-600
                p-1
              "
            />
          </div>
        </div>
        <div class="flex items-center lg:hidden">
          <input
            type="search"
            placeholder="Search Location"
            class="
              h-16
              w-full
              rounded-lg
              border-2 border-indigo-100
              px-4
              placeholder:text-xs
            "
          />
          <SearchIcon
            class="
              -ml-12
              h-10
              w-10
              rounded-sm
              bg-indigo-600
              stroke-indigo-100
              p-1
            "
          />
        </div>
        <div
          class="
            hidden
            h-24
            w-full
            items-center
            gap-4
            rounded-lg
            border-2 border-indigo-100
            px-4
            font-inter
            lg:flex
          "
        >
          <div class="w-1/2 min-w-max border-r-2 border-gray-300 px-4">
            <span class="text-base text-gray-900">Location</span>
            <p class="text-lg font-bold">New York, USA</p>
          </div>
          <div class="w-1/2 min-w-max border-r-2 border-gray-300 px-4">
            <span class="text-base text-gray-900">When</span>
            <p class="text-lg font-bold">Select Move-in Date</p>
          </div>
          <div class="w-1/2 min-w-max border-r-2 border-gray-300 px-4 pr-10">
            <span class="text-base text-gray-900">Price</span>
            <p class="text-lg font-bold">$500-$2,500</p>
          </div>
          <div class="flex w-1/2 items-center justify-center">
            <p
              class="
                rounded-sm
                bg-indigo-600
                px-6
                py-3
                text-center text-indigo-100
              "
            >
              Search
            </p>
          </div>
        </div>
      </div>
      <div
        class="
          mx-auto
          grid
          w-4/5
          grid-cols-[repeat(auto-fit,minmax(300px,1fr))]
          justify-center
          gap-7
        "
      >
        <Card :price="2500" :favori="true" :image="'src/assets/house2.png'" />
        <Card
          :price="2850"
          :adresse="'2820 Lake Sevilla, Palm Harbor, TX'"
          :image="'/public/house3.jpg'"
        />
        <Card
          :price="4500"
          :favori="true"
          :adresse="'2820 Lake Sevilla, Palm Harbor, TX'"
          :image="'/public/house.png'"
        />
        <Card
          :price="2850"
          :adresse="'2820 Lake Sevilla, Palm Harbor, TX'"
          :image="'/public/house4.jpg'"
        />
        <Card
          :price="2850"
          :adresse="'2820 Perdu dans la nature'"
          :image="'/public/house5.jpg'"
        />
        <Card :price="2500" :favori="true" :image="'/public/house2.png'" />
        <Card
          :price="2850"
          :adresse="'2820 Lake Sevilla, Palm Harbor, TX'"
          :image="'/public/house3.jpg'"
        />
        <Card
          :price="4500"
          :favori="true"
          :adresse="'2820 Lake Sevilla, Palm Harbor, TX'"
          :image="'/public/house.png'"
        />
        <Card
          :price="2850"
          :adresse="'2820 Lake Sevilla, Palm Harbor, TX'"
          :image="'/public/house4.jpg'"
        />
        <Card
          :price="2850"
          :adresse="'2820 Lake Sevilla, Perl Harbor, TX'"
          :image="'/public/house5.jpg'"
        />
      </div>
    </main>
    <footer>
      <div class="flex flex-col pt-4 lg:flex-row">
        <div class="mx-16 mb-8 mt-3 flex items-center">
          <HomeIcon class="w-8 fill-indigo-500" />
          <span class="font-semibold">Estatery</span>
        </div>
        <div class="mx-5 flex w-full gap-28 pb-16 lg:flex-col">
          <div
            class="flex flex-col gap-3 lg:w-full lg:flex-row lg:justify-around"
          >
            <div class="flex flex-col">
              <p class="text-base font-semibold">Sell A Home</p>
              <span class="text-xs text-gray-400">Request an offer</span>
              <span class="text-xs text-gray-400">Pricing</span>
              <span class="text-xs text-gray-400">Reviews</span>
              <span class="text-xs text-gray-400">Stories</span>
            </div>
            <div class="flex flex-col">
              <p class="text-base font-semibold">Buy A Home</p>
              <span class="text-xs text-gray-400">Buy</span>
              <span class="text-xs text-gray-400">Finance</span>
            </div>
            <div class="flex flex-col">
              <p class="text-base font-semibold">Buy, Rent and Sell</p>
              <span class="text-xs text-gray-400">Buy & sell properties</span>
              <span class="text-xs text-gray-400">Rent home</span>
              <span class="text-xs text-gray-400">Builder trade-up</span>
            </div>
          </div>
          <div
            class="flex flex-col gap-3 lg:w-full lg:flex-row lg:justify-around"
          >
            <div class="flex flex-col">
              <p class="text-base font-semibold">Terms & Privacy</p>
              <span class="text-xs text-gray-400">Trust & Safety</span>
              <span class="text-xs text-gray-400">Terms of Service</span>
              <span class="text-xs text-gray-400">Privacy Policy</span>
            </div>
            <div class="flex flex-col">
              <p class="text-base font-semibold">About</p>
              <span class="text-xs text-gray-400">Company</span>
              <span class="text-xs text-gray-400">How it works</span>
              <span class="text-xs text-gray-400">Contact</span>
              <span class="text-xs text-gray-400">Investitor</span>
            </div>
            <div class="flex flex-col">
              <p class="text-base font-semibold">Resources</p>
              <span class="text-xs text-gray-400">Blog</span>
              <span class="text-xs text-gray-400">Guides</span>
              <span class="text-xs text-gray-400">FAQ</span>
              <span class="text-xs text-gray-400">Help Center</span>
            </div>
          </div>
        </div>
      </div>
      <div
        class="
          my-10
          flex flex-col
          items-center
          justify-center
          gap-2
          border-t border-t-indigo-100
          pt-10
          lg:flex-row
        "
      >
        <span class="text-xs text-gray-400"
          >2021 Estatery. All rights reserved</span
        >
        <span class="flex items-center gap-4">
          <insta class="w-4" />
          <fb class="w-4" />
          <twitter class="w-4" />
          <linkedin class="w-5" />
        </span>
      </div>
    </footer>
  </div>
</template>
<style >
.bouton1 {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 12px 24px;
  background: #6366f1;
  border-radius: 8px;
}
.bouton2 {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 10px 22px;
  border: 2px solid #c7d2fe;
  border-radius: 8px;
}
.menu {
  display: block;
}
.menu-text {
  display: none;
  align-items: center;
}
/** média **/
@media screen and (min-width: 1024px) {
  .menu {
    display: none;
  }
  .menu-text {
    display: flex;
  }
}
</style>
 
<script >
import Card from "./components/Card.vue";
import { HomeIcon } from "@heroicons/vue/solid";
import { MenuIcon, ChevronDownIcon, SearchIcon } from "@heroicons/vue/outline";
import insta from "./components/icones/insta.vue";
import fb from "./components/icones/fb.vue";
import twitter from "./components/icones/twitter.vue";
import linkedin from "./components/icones/linkedin.vue";

export default {
  name: "App",
  components: {
    Card,
    HomeIcon,
    MenuIcon,
    insta,
    fb,
    twitter,
    linkedin,
    ChevronDownIcon,
    SearchIcon,
  },
  data() {
    return {
      MenuOpen: false,
    };
  },
};
</script>

