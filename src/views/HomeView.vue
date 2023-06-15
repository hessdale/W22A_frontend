<template>
  <div>
  <all-candy></all-candy>
  <new-candy></new-candy>
  <delete-candy></delete-candy>
  </div>
</template>

<script>
// @ is an alias to /src
import AllCandy from '@/components/AllCandy.vue'
import NewCandy from '@/components/NewCandy.vue'
import DeleteCandy from '@/components/DeleteCandy.vue'

export default {
  name: 'HomeView',
  components: {
    AllCandy,NewCandy,DeleteCandy
  }
}
</script>
