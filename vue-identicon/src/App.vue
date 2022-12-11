<template>
  <div class="py-4 w-full mx-auto text-center">
    <h1 class="text-2xl bold">Vue Identicon</h1>
    <identicon-item></identicon-item>
  </div>
</template>
<script>
import IdenticonItem from "@/components/IdenticonItem.vue";
export default {
  components:{
    IdenticonItem
  }
}
</script>
