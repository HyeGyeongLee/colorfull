<template>
    <div class="bg-white py-6 md:py-32 md:px-0 px-6 mb-12">
      <div class="mx-auto grid max-w-7xl">
        <div class="max-w-4xl mb-12">
          <h2 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">아드모의 두번째 전시회</h2>
          <p class="mt-6 text-lg font-bold">COLORFULL</p>
          <p class="mt-3 text-lg leading-8 text-gray-600 break-keep text-justify">종로 미루 갤러리 - 2025.03</p>
        </div>
        <ul role="list" class="-mt-12 space-y-12 divide-y divide-gray-200 xl:col-span-3">
          <li v-for="person in people" :key="person.name" class="flex flex-col gap-10 pt-12 sm:flex-row">
            <img class="w-[30%] flex-none rounded-2xl object-cover" :src="person.imageUrl" alt="" />
            <div class="max-w-3xl flex-auto relative">
              <h3 class="text-lg font-semibold leading-8 tracking-tight text-gray-900">{{ person.name }}</h3>
              <p class="text-base leading-7 text-gray-600">{{ person.role }}</p>
              <p class="mt-6 sm:text-base sm:leading-9 text-sm leading-6  text-gray-600 break-keep text-justify">{{ person.bio }}</p>
              <ul role="list" class="mt-6 flex gap-x-6">
                <li>
                    <p class="text-gray-600 text-base">wingedant1@naver.com</p>
                </li>
                <li>
                  <a :href="person.linkedinUrl" target='_blank' class="text-gray-400 hover:text-gray-500">
                    <span class="sr-only">LinkedIn</span>
                    <svg class="h-5 w-5" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M16.338 16.338H13.67V12.16c0-.995-.017-2.277-1.387-2.277-1.39 0-1.601 1.086-1.601 2.207v4.248H8.014v-8.59h2.559v1.174h.037c.356-.675 1.227-1.387 2.526-1.387 2.703 0 3.203 1.778 3.203 4.092v4.711zM5.005 6.575a1.548 1.548 0 11-.003-3.096 1.548 1.548 0 01.003 3.096zm-1.337 9.763H6.34v-8.59H3.667v8.59zM17.668 1H2.328C1.595 1 1 1.581 1 2.298v15.403C1 18.418 1.595 19 2.328 19h15.34c.734 0 1.332-.582 1.332-1.299V2.298C19 1.581 18.402 1 17.668 1z" clip-rule="evenodd" />
                    </svg>
                  </a>
                </li>
              </ul>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </template>
  
  <script setup>
  const people = [
    {
      name: '',
      role: '',
      imageUrl:
        '/about.jpeg',
      bio: `우리끼리 만드는 작은 전시회. 서로 다른 모습과 생각을 가진 우리들이 모여 각자의 이야기를 펼쳐냅니다. 누군가는 선명한 빨강으로, 또 다른 이는 차분한 파랑으로 자신만의 색깔을 표현합니다. 때로는 대비되고, 때로는 부드럽게 어우러지는 우리들의 모습처럼, 이 전시는 다양한 개성의 조화를 보여줍니다. 서로의 다름을 인정하고 존중하며 발견하는 특별한 아름다움, 그 순간을 관람객 여러분과 함께 나누고자 합니다. 우리들의 작은 이야기가 모여 만드는 다채로운 전시에 여러분을 초대합니다.
      `,
      linkedinUrl: 'https://www.instagram.com/bamzrara_/',
    },

    // {
    //   name: 'HyeGyeong Lee',
    //   role: 'Frontend Developer',
    //   imageUrl:
    //     '/about.jpeg',
    //   bio: `
    //   인간의 가장 순수하고 강렬한 감정인 '환희'를 인물화에 담아냅니다. 기쁨이 절정에 달했을 때 우리의 얼굴은 어떤 모습일까요? 환한 미소 너머 빛나는 눈동자, 들뜬 마음이 그대로 전해지는 표정, 축제처럼 피어나는 감정의 순간들을 캔버스에 포착했습니다. 때로는 강렬하게, 때로는 은은하게 표현된 다양한 얼굴들은 각기 다른 이야기를 품고 있지만, 모두가 공통된 '환희'라는 감정으로 연결됩니다. 일상 속 특별한 순간, 예기치 않은 기쁨, 오랫동안 기다려온 설렘이 폭발하는 그 찰나의 표정들을 만나보세요. 환희에 찬 얼굴들이 전하는 따뜻한 공감과 위로를 이번 전시를 통해 나누고자 합니다.
    //   `,
    //   linkedinUrl: 'https://www.instagram.com/bamzrara_/',
    // },
    // More people...
  ]
  </script>