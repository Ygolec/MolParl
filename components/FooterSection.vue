<template>
  <div class="col-span-6 md:col-span-3 lg:col-span-2">
    <div class="text-gray-800 dark:text-gray-300 font-medium mb-2">{{ name }}</div>
    <ul class="text-sm">
      <li v-for="link of links" class="mb-2">
        <a href={{link.text}}
           class="text-gray-600 hover:text-gray-700 dark:text-gray-400 transition duration-150 ease-in-out"
        >{{ link.text }}</a
        >
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
interface Props {
  name: string,
  links: Array<{
    text: string,
    href: string
  }>
}

const props = defineProps<Props>()
</script>

<style scoped lang="scss">

</style>