<template>
        <figure class="m-5 pb-5 bg-gray-50 grid grid-flow-row-dense  grid-cols-3 rounded-xl">
            <img class="w-full h-48 object-cover col-span-3 rounded-t-xl" :src="image" alt="" />

            <figcaption class="relative border-2 border-t-0 rounded-lg contents">

                <section class="contents ">
                    <div class="contents ">
                        <div class=" pl-5 text-xl font-bold text-left text-indigo-500 col-span-1">${{ price }}
                        <div class=" text-gray-500 text-base inline-block col-span-2">/month</div></div>
                        <div class="pl-5 rounded-full mt-2 flex place-content-end">
                            <heart :class="{ 'fill-rose-600': favori }" />
                        </div>
                    </div>
                    <h3 class="text-xl pl-5 text-gray-900 col-span-3 ">{{ location }}</h3>
                    <div class="text-gray-500 pl-5 col-span-3 mb-6 mt-2">{{ adress }}</div>
                    <hr class="pl-5 border-indigo-100 m-6 " />
                    <div class=" text-sm contents">
                        <div class="w-max pl-5"><bed class="h-5 w-5 mr-1 inline-block col-span-1"/>{{nbrbed}} Beds</div>
                        <div class="w-max pl-5"><bath class="h-5 w-5 mr-1 inline-block col-span-1"/>{{nbrbath}} Bath</div>
                        <div class="w-max pl-5"><dimensions class="h-5 w-5 mr-1 inline-block col-span-1"/>{{ size }}</div>
                    </div>
                </section>
            </figcaption>
        </figure>
</template>

<script>
import dimensions from "./icones/dimensions.vue";
import bed from "./icones/beds.vue";
import bath from "./icones/bath.vue";
import heart from "./icones/heart.vue";

export default {
  props: {
    location: String,
    adress: String,
    price: Number,
    favori: Boolean,
    image: String,
    nbrbath: Number,
    nbrbed: Number,
    size: String
  },
  components: { bath, heart, bed, dimensions },
};
</script>