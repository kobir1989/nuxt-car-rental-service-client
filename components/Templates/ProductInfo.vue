<script setup>
import { landingPageProducts as products } from "~/constants/products";
</script>

<template>
  <MainContainer class="intersection">
    <!-- title & description -->
    <div class="flex flex-col lg:flex-row gap-[2rem] mt-[5rem]">
      <SectionTitle
        >What We Provide Is The Luxury Transport And Most Comfortable
        Experience.</SectionTitle
      >
      <div>
        <p class="text-gray-200 leading-7 tracking-[0.5px]">
          Experience the epitome of luxury in transportation. We offer the most
          comfortable and opulent journeys, setting new standards in travel.
          Discover a world of relaxation and style with us.
        </p>
        <p
          class="mt-6 text-gold-900 font-inconso text-md font-bold tracking-[2px] flex items-center gap-3"
        >
          <span class="text-[3rem]">
            <CustomarCare />
          </span>
          CALL CENTER: +880174000000
        </p>
      </div>
    </div>
    <!-- Product Cards  -->
    <div
      class="mt-[5rem] grid gird lg:grid-cols-3 sm:grid-cols-2 grid-cols-1 justify-items-center gap-x-4 gap-y-12"
    >
      <div
        v-for="product in products"
        :key="product.id"
        class="w-full intersection"
      >
        <PricingCard
          :name="product?.name"
          :lebel="product?.label"
          :description="product?.description"
          :image="product?.image"
          :rating="product?.rating"
          :price="product?.price"
        />
      </div>
    </div>
  </MainContainer>
</template>
~/constants/products
