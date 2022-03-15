<script setup>
const colorMode = useColorMode()
</script>

<template>
  <div class="container mx-auto pt-4">
    <Html lang="en" />
    <Meta name="description" content="Sfeir demo app with Nuxt 3, listing mountains" />
    <select v-model="colorMode.preference" class="fixed right-2 bottom-2">
      <option value="system">System</option>
      <option value="light">Light</option>
      <option value="dark">Dark</option>
    </select>
    <NuxtPage/>
  </div>
</template>

<style lang="postcss">
.dark body {
  @apply bg-black text-white;
}
.dark select {
  @apply bg-gray-800;
}
</style>