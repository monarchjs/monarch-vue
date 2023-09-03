<script lang="ts" setup>
import { reactive } from 'vue'

export interface Props {
  label?: string
}

const props = withDefaults(defineProps<Props>(), {
  label: 'hello',
})

const { label } = reactive(props)
</script>

<template>
  <button>
    {{ label }}
  </button>
</template>

<style scoped>
button {
  padding: 0.6rem 1.25rem;
  background-color: var(--mon-btn-primary, #646cff);
  border: 0;
}
button:hover {
  background-color: #535bf2;
}
</style>
