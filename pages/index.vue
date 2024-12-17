<template>
  <div class="bg-[#f7f1f0] py-0 sm:py-0">
    <div class="mx-auto">
      <div class="relative">
          <swiper
            :modules="[SwiperAutoplay, SwiperPagination, SwiperNavigation, SwiperEffectFade]"
            :loop="true"
            :slides-per-view="1"
            :space-between="10"
            :centered-slides="true"
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
                slidesPerView: 3,
                spaceBetween: 10
              }
            }"
            class="w-full mt-0"
          >
            <swiper-slide v-for="person in people" :key="person.imageUrl" class="">
              <div class="">
                <img 
                  :src="person.imageUrl" 
                  alt="" 
                  class="xl:h-[90vh]"
                />
              </div>
            </swiper-slide>
          </swiper>
      </div>
      <div class="text-sm xl:text-2xl text-center xl:py-44 py-6 bg-[#F266B3] text-gray-50">
        <div class="font-bold mb-2 text-xl xl:text-4xl xl:mb-6">우리끼리 만드는 작은 전시회</div>
        <div>서로 다른 사람들, 서로 다른 색깔로</div>
        <div>조화롭게 온 세상을 가득 채우고 싶은</div>
        <div>마음들이 모였습니다.</div>
      </div>

      <div>
        <img src="/main/aaina-sharma-nqj3ncOPS0g-unsplash.jpg"/>
      </div>

      <!-- 
        <button 
          type="button" 
          class="text-[#F2059F] font-bold bg-white/50 xl:text-3xl text-[0.6rem] border-solid border-2 border-[#F2059F] rounded-full xl:px-12 px-3 xk:py-2 absolute xl:bottom-[5vh] bottom-[4%] left-1/2 -translate-x-1/2"
        >
          About
        </button> -->
    </div>
  </div>
</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Autoplay, Pagination, Navigation, EffectFade } from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/navigation';
import 'swiper/css/effect-fade';

// Swiper modules
const SwiperAutoplay = Autoplay;
const SwiperPagination = Pagination;
const SwiperNavigation = Navigation;
const SwiperEffectFade = EffectFade;

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