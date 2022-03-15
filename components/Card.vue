<script setup>
const props = defineProps({
  title: String,
  image: String,
  description: String
})
</script>

<template>
  <article class="p-4 border dark:border-gray-700 clear-both overflow-hidden rounded mb-4">
    <img class="float-right h-20 ml-4" :src="props.image" :alt="props.title" />
    <section>
      <h2 class="text-2xl dark:text-white">{{ props.title }}</h2>
      <p class="text-gray-600 dark:text-gray-400">{{ props.description }}</p>
    </section>
  </article>
</template>