<template>
  <div class="bg-gradient-to-br from-[#E8E3E2] to-[#ffffff] py-0 sm:py-0">
    <div class="mx-auto py-6">
      <div class="relative xl:flex">
        <div class="ml-2 xl:ml-[10%] mb-12 break-keep">
            <!-- <div class="xl:text-[7rem] text-[2.5rem] leading-tight font-bold xl:mt-[10%] mt-12">
              <div class="text-[#F2059F]">I.D.MO</div>
              <div class="text-[#da289c]">SECOND</div>
              <div class="text-[#b0207e]">EXHIBITION</div>
            </div> -->

            <div class="font-[Calligraffitti] font-bold xl:text-[8rem] text-[4rem] tracking-[0.02em] text-[#ffe77d]" style="text-shadow: 5px 5px 0px #FFB650, 
              10px 10px 0px #FFD662, 
              15px 15px 0px #FF80BF, 
              20px 20px 0px #EF5097, 
              25px 25px 0px #6868AC, 
              30px 30px 0px #90B1E0;">
              <div>I.D.MO</div>
              <div>SECOND</div>
              <div>EXHIBITION</div>
              <div >COLORFULL</div>
            </div>

            <!-- <div class="text-black xl:text-[8rem] text-[4rem] font-bold">
              <div>I.D.MO</div>
              <div>SECOND</div>
              <div>EXHIBITION</div>
              <div >COLORFULL</div>
            </div> -->
        </div>
          <swiper
            :modules="[SwiperAutoplay, SwiperPagination, SwiperNavigation, SwiperEffectFade]"
            :loop="true"
            :slides-per-view="1"
            :space-between="10"
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
            class="w-full mt-0 float-right"
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

      

      <!-- <div>
        <img src="/main/aaina-sharma-nqj3ncOPS0g-unsplash.jpg"/>
      </div> -->

      <!-- 
        <button 
          type="button" 
          class="text-[#F2059F] font-bold bg-white/50 xl:text-3xl text-[0.6rem] border-solid border-2 border-[#F2059F] rounded-full xl:px-12 px-3 xk:py-2 absolute xl:bottom-[5vh] bottom-[4%] left-1/2 -translate-x-1/2"
        >
          About
        </button> -->

        <div class="text-white text-center bg-gradient-to-br from-[#A9C9FF] to-[#FFBBEC] py-40">
              <div class="text-[2em] font-bold mb-4 xl:mt-0 mt-[34rem]">우리끼리 만드는 작은 전시회</div>
              <div class="text-[1.5em]">서로 다른 사람들, 서로 다른 색깔로</div>
              <div class="text-[1.5em]">조화롭게 온 세상을 가득 채우고 싶은</div>
              <div class="text-[1.5em]">마음들이 모였습니다.</div>
          </div>

            <div class="">
                  <div class="text-4xl text-center py-12">ARTIST</div>
                  <div class="h-full xl:py-12 grid xl:grid-cols-3 grid-cols-2">
                      <div 
                          v-for="person in people2" 
                          :key="person.id" 
                          class="max-w-[800px] rounded-md shadow-2xl xl:overflow-hidden mb-8 mx-auto xl:w-[25rem] w-[11rem] bg-white"
                        >
                      <div>
                        <img :src="person.imageUrl" :alt="person.nickname" class="w-[30rem] block">
                      </div>
                      <div class="bg-white flex-1 p-8 flex flex-col">
                        <div class="xl:flex items-center mb-5">
                          <h1 class="text-base mr-auto text-blue-600">{{ person.nickname }} <i class="fas fa-fire text-salmon"></i></h1>
                          <!-- <div v-for="tag in person.hashtags" :key="tag" 
                              class="text-xs text-white px-2 py-0.5 rounded-full mr-2 uppercase"
                              :class="tag.includes('1') ? 'bg-[#A9C9FF]' : 'bg-[#FFBBEC]'">
                            {{ tag }}
                          </div> -->
                        </div>
                        <p class="text-sm">
                          {{ person.introduction }}
                        </p>
                      </div>
                        <div class="bg-gradient-to-b from-[#A9C9FF] to-[#FFBBEC] flex-[0_0_50px] text-lg font-bold tracking-wider text-white [writing-mode:vertical-lr] flex items-center justify-center">
                        </div>
                   </div>
                  </div>
            </div>

            <div class="w-full xl:w-[40rem] m-auto">
              <div class="text-4xl text-center py-12">D_DAY</div>
            <!-- Calendar Header with Select Options -->
            <div class="bg-white grid grid-cols-2 gap-4 rounded-t-[34px] p-5">
              <div class="bg-gray-100 px-5 py-4 rounded-[20px] font-bold text-[1.02rem] appearance-none bg-[right_20px_center] bg-no-repeat cursor-pointer outline-none">
                <option selected>3월</option>
              </div>
              <div class="bg-gray-100 px-5 py-4 rounded-[20px] font-bold text-[1.02rem] appearance-none bg-[right_20px_center] bg-no-repeat cursor-pointer outline-none">
                <option selected>2025</option>
              </div>
            </div>

            <!-- Calendar Body -->
            <div class="bg-gradient-to-b from-gray-100 to-white">
              <!-- Days Header -->
              <div class="bg-white grid grid-cols-7 px-5 pb-2.5">
                <div v-for="day in ['일', '월', '화', '수', '목', '금', '토']" 
                    class="text-center font-bold text-[1.02rem] text-gray-400">
                  {{ day }}
                </div>
              </div>

              <!-- Calendar Dates -->
              <div class="grid grid-cols-7 p-5">
                <!-- Previous Month Dates (Grey) -->
                <div v-for="date in prevDates" 
                    class="text-center h-[46.6px] leading-[46.6px] font-semibold text-[1.02rem] text-gray-400 cursor-not-allowed">
                  <span class="relative z-10">{{ date }}</span>
                </div>

                <!-- Current Month Dates -->
                <div v-for="date in 31" 
                    :class="[
                      'text-center h-[46.6px] leading-[46.6px] font-semibold text-[1.02rem] cursor-pointer relative group',
                      date >= 3 && date <= 9 ? 'text-[#ff374b]' : ''
                    ]">
                  <span class="relative z-10">{{ date }}</span>
                  <div v-if="date >= 3 && date <= 9" 
                      :class="[
                        'absolute inset-0 top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-full h-[90%] bg-[#ffeaec]',
                        date === 3 ? 'rounded-l-[15px]' : '',
                        date === 9 ? 'rounded-r-[15px]' : ''
                      ]"></div>
                  <div v-else class="absolute inset-0 top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-full h-[90%] bg-gray-200 opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-[15px]"></div>
                </div>
              </div>
            </div>

            <!-- Calendar Footer -->
            <div class="bg-white grid grid-cols-2 gap-4 rounded-b-[34px] p-5">
              <button class="bg-gray-100 px-5 py-4 rounded-[20px] font-bold text-[1.02rem]">
                Back
              </button>
              <button class="bg-[#1752ff] text-white px-5 py-4 rounded-[20px] font-bold text-[1.02rem] transition-all duration-300 hover:shadow-[0_20px_30px_-13px_rgba(23,82,255,0.45)] hover:-translate-y-[3px] active:shadow-[0_10px_10px_-6px_rgba(23,82,255,0.45)] active:-translate-y-[1px]">
                Apply
              </button>
            </div>
          </div>
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

const people2 = [
  {
    id: 1,
    nickname: "행복한 사자",
    imageUrl: "https://www.mensjournal.com/wp-content/uploads/2018/10/rambo-main-3.jpg?quality=86&strip=all",
    hashtags: ["#열정", "#긍정"],
    introduction: "안녕하세요! 항상 긍정적인 마인드로 살아가려 노력하는 행복한 사자입니다."
  },
  {
    id: 2,
    nickname: "꿈꾸는 돌고래",
    imageUrl: "https://www.mensjournal.com/wp-content/uploads/2018/10/rambo-main-3.jpg?quality=86&strip=all",
    hashtags: ["#창의", "#도전"],
    introduction: "새로운 도전을 즐기는 꿈꾸는 돌고래입니다. 창의적인 아이디어로 세상을 바꾸고 싶어요."
  },
  {
    id: 3,
    nickname: "춤추는 나비",
    imageUrl: "https://www.mensjournal.com/wp-content/uploads/2018/10/rambo-main-3.jpg?quality=86&strip=all",
    hashtags: ["#자유", "#예술"],
    introduction: "예술을 사랑하는 자유로운 영혼의 소유자입니다. 삶을 춤추듯 살아가고 싶어요."
  },
  {
    id: 4,
    nickname: "생각하는 부엉이",
    imageUrl: "https://www.mensjournal.com/wp-content/uploads/2018/10/rambo-main-3.jpg?quality=86&strip=all",
    hashtags: ["#지혜", "#성장"],
    introduction: "끊임없이 배우고 성장하는 것을 좋아하는 생각하는 부엉이입니다."
  },
  {
    id: 5,
    nickname: "노래하는 종달새",
    imageUrl: "https://www.mensjournal.com/wp-content/uploads/2018/10/rambo-main-3.jpg?quality=86&strip=all",
    hashtags: ["#음악", "#희망"],
    introduction: "음악으로 세상을 더 아름답게 만들고 싶은 노래하는 종달새입니다."
  },
  {
    id: 6,
    nickname: "노래하는 종달새",
    imageUrl: "https://www.mensjournal.com/wp-content/uploads/2018/10/rambo-main-3.jpg?quality=86&strip=all",
    hashtags: ["#음악", "#희망"],
    introduction: "음악으로 세상을 더 아름답게 만들고 싶은 노래하는 종달새입니다."
  },
  {
    id: 7,
    nickname: "노래하는 종달새",
    imageUrl: "https://www.mensjournal.com/wp-content/uploads/2018/10/rambo-main-3.jpg?quality=86&strip=all",
    hashtags: ["#음악", "#희망"],
    introduction: "음악으로 세상을 더 아름답게 만들고 싶은 노래하는 종달새입니다."
  },
  {
    id: 8,
    nickname: "노래하는 종달새",
    imageUrl: "https://www.mensjournal.com/wp-content/uploads/2018/10/rambo-main-3.jpg?quality=86&strip=all",
    hashtags: ["#음악", "#희망"],
    introduction: "음악으로 세상을 더 아름답게 만들고 싶은 노래하는 종달새입니다."
  },
  {
    id: 9,
    nickname: "노래하는 종달새",
    imageUrl: "https://www.mensjournal.com/wp-content/uploads/2018/10/rambo-main-3.jpg?quality=86&strip=all",
    hashtags: ["#음악", "#희망"],
    introduction: "음악으로 세상을 더 아름답게 만들고 싶은 노래하는 종달새입니다."
  },
  {
    id: 10,
    nickname: "노래하는 종달새",
    imageUrl: "https://www.mensjournal.com/wp-content/uploads/2018/10/rambo-main-3.jpg?quality=86&strip=all",
    hashtags: ["#음악", "#희망"],
    introduction: "음악으로 세상을 더 아름답게 만들고 싶은 노래하는 종달새입니다."
  }
];

const prevDates = [25, 26, 27, 28, 29, 30];
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

/* select {
  background-image: url("data:image/svg+xml,%3C%3Fxml version='1.0' encoding='utf-8'%3F%3E%3C!DOCTYPE svg PUBLIC '-//W3C//DTD SVG 1.1//EN' 'http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd'%3E%3Csvg version='1.1' id='Capa_1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink' x='0px' y='0px' width='960px' height='560px' viewBox='0 0 960 560' enable-background='new 0 0 960 560' xml:space='preserve'%3E%3Cg id='Rounded_Rectangle_33_copy_4_1_'%3E%3Cpath d='M480,344.181L268.869,131.889c-15.756-15.859-41.3-15.859-57.054,0c-15.754,15.857-15.754,41.57,0,57.431l237.632,238.937 c8.395,8.451,19.562,12.254,30.553,11.698c10.993,0.556,22.159-3.247,30.555-11.698l237.631-238.937 c15.756-15.86,15.756-41.571,0-57.431s-41.299-15.859-57.051,0L480,344.181z'/%3E%3C/g%3E%3C/svg%3E");
  background-size: 24px;
} */
</style>