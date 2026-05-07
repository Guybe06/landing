<script setup lang="ts">
const links = [
  { label: 'Documentation', to: '#' },
  { label: 'Tarifs', to: '#' },
  { label: 'Roadmap', to: '#' },
  { label: 'Communaute', to: '#' },
  { label: 'Confidentialite', to: '#' }
]
</script>

<template>
  <UFooter
    :ui="{
      container: 'border-t border-default lg:py-8',
      right: 'gap-x-0 flex-wrap'
    }"
  >
    <template #left>
      <p class="text-sm text-dimmed">
        &copy; {{ new Date().getFullYear() }} Skema. Developpe par Winsa Ltd
      </p>
    </template>

    <template #right>
      <UButton
        v-for="link in links"
        :key="link.label"
        :label="link.label"
        :to="link.to"
        color="neutral"
        variant="link"
        class="font-light"
        size="sm"
      />
    </template>
  </UFooter>
</template>
