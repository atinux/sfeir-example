<script setup>
const { params } = useRoute()
const { data: mountain } = await useFetch(`https://api.nuxtjs.dev/mountains/${params.slug}`)
</script>

<template>
  <div >
    <NuxtLink to="/" class="underline block pb-4">Back to mountains</NuxtLink>
    <div v-if="mountain">
      <Title>Mountain: {{ mountain.title }}</Title>
      <img :src="mountain.image" :alt="mountain.title" />
      <h1 class="text-4xl mt-2">{{ mountain.title }}</h1>
      <p>{{ mountain.description }}</p>
    </div>
    <h1 v-else class="text-4xl mt-2">Mountain not found</h1>
  </div>
</template>