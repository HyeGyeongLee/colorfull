<template>
    <div class="bg-white py-0 sm:py-0">
      <div class="mx-auto px-6 lg:px-8">
        
        <ul role="list" class="mx-auto mt-0 grid max-w-2xl grid-cols-2 gap-x-1 gap-y-1 sm:grid-cols-2 lg:mx-0 lg:max-w-none lg:grid-cols-4">
          <li v-for="person in people" :key="person.name">
            <img class="w-[100%] h-full" :src="person.imageUrl" alt="" />
          </li>
        </ul>
      </div>
    </div>
  </template>
  
  <script setup>
  const people = [
  {
      imageUrl:
        '/work/work9.jpeg',
    },
  {
      imageUrl:
        '/work/work8.jpeg',
    },
  {
      imageUrl:
        '/work/work7.jpeg',
    },
  {
      imageUrl:
        '/work/work6.jpeg',
    },
  {
      imageUrl:
        '/work/work5.jpeg',
    },
  {
      imageUrl:
        '/work/work4.jpeg',
    },
  {
      imageUrl:
        '/work/work3.jpeg',
    },
  {
      imageUrl:
        '/work/work2.jpeg',
    },
  {
      imageUrl:
        '/work/work1.jpeg',
    },
    {
      imageUrl:
        '/main/main1.jpeg',
    },
    {
      imageUrl:
        '/main/main2.jpeg',
    },
    {
      imageUrl:
        '/main/main3.jpeg',
    },
    {
      imageUrl:
        '/main/main4.jpeg',
    },
    {
      imageUrl:
        '/main/main5.jpeg',
    },
    {
      imageUrl:
        '/main/main6.jpeg',
    },
    {
      imageUrl:
        '/main/main7.jpeg',
    },
    {
      imageUrl:
        '/main/main8.jpeg',
    },
    // More people...
  ]
  </script>