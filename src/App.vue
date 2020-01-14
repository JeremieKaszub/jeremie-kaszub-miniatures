<template>
  <div id="app">
    <TwoColumns>
      <template v-slot:aside> <Menu /> </template>
      <template v-slot:main> <router-view /></template>
    </TwoColumns>
  </div>
</template>

<script>
import TwoColumns from "@/components/ui/TwoColumns.vue";

import Menu from "@/components/navigation/Menu.vue";

export default {
  components: {
    TwoColumns,
    Menu
  }
};
</script>
