<script setup lang="ts">
import { Person } from './Person'

interface Props {
  person: Person
  age: number
}

defineProps<Props>()

defineEmits<{
  (event: 'selected', name: string): void
  (event: 'deleted'): void
  (event: 'updated'): void
}>()
</script>

<template>
  <q-page class="row items-center justify-evenly">
    <!--  -->
  </q-page>
</template>
