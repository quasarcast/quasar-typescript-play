<script lang="ts" setup>
import { computed } from 'vue'
import IndexPage from './IndexPage.vue'
import { Person } from './Person'

const personFetcher = useFetchResources(Person, { immediate: true })
const personRepo = useRepo(Person)

const marcFriends = computed(() => {
  return personRepo.query().with('friends').friends
})

marcFriends.value[0]?.name || 'nigel no friends'

function onButtonClicked (name: string) {
  console.log(name)
}
</script>

<template>
  <IndexPage
    :age="5345"
    :person="person"
    @selected="onButtonClicked"
  />
</template>
