<template>
  <div class="bg-[#E8E3E2] py-0 sm:py-0 xl:max-w-[80rem] xl:m-auto">
    <div class="mx-auto px-6 lg:px-8">
      <swiper
        :modules="[SwiperAutoplay, SwiperPagination, SwiperNavigation]"
        :slides-per-view="1"
        :space-between="10"
        :centered-slides="true"
        :navigation="true"
        :pagination="{ clickable: true }"
        :autoplay="{
          delay: 3000,
          disableOnInteraction: false,
        }"
        :breakpoints="{
          320: {
            slidesPerView: 1,
            spaceBetween: 10
          },
          640: {
            slidesPerView: 1,
            spaceBetween: 10
          },
          1024: {
            slidesPerView: 1,
            spaceBetween: 10
          }
        }"
        class="w-full"
      >
        <swiper-slide v-for="person in people" :key="person.imageUrl" class="xl:flex items-center justify-center">
          <div class="w-full flex items-center justify-center">
            <img 
              :src="person.imageUrl" 
              alt="" 
              class="xl:h-[90vh] w-auto object-contain mx-auto"
            />
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </div>
</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Autoplay, Pagination, Navigation } from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/navigation';

// Swiper modules
const SwiperAutoplay = Autoplay;
const SwiperPagination = Pagination;
const SwiperNavigation = Navigation;

const people = [
  {
    imageUrl: '/main/11.png',
  },
  {
    imageUrl: '/main/22.png',
  },
  {
    imageUrl: '/main/33.png',
  },
  {
    imageUrl: '/main/44.png',
  },
];
</script>

<style>
.swiper-button-next,
.swiper-button-prev {
  color: #000 !important;
}

.swiper-pagination-bullet-active {
  background: #000 !important;
}

.swiper-slide {
  display: flex !important;
  align-items: center !important;
  justify-content: center !important;
}
</style>