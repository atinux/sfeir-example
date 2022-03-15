<script setup>
const { data: mountains } = await useFetch('https://api.nuxtjs.dev/mountains')
useMeta({
  title: 'Sfeir - Mountains',
  description: 'A list of mountains for Sfeir talk'
})
</script>

<template>
  <main>
    <h1 class="text-3xl mb-4">Hello Sfeir!</h1>
    <NuxtLink v-for="mountain of mountains" :to="`/mountains/${mountain.slug}`">
      <Card
        :title="mountain.title"
        :image="mountain.image"
        v-bind:description="mountain.description"
      />
    </NuxtLink>
  </main>
</template>
