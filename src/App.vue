<template>
  <div id="app">
    <Header />
    <TwoColumns>
      <template v-slot:aside> <Menu /> </template>
      <template v-slot:main> <router-view /></template>
    </TwoColumns>
  </div>
</template>

<script>
import Header from "@/components/global/Header.vue";
import TwoColumns from "@/components/ui/TwoColumns.vue";
import Menu from "@/components/navigation/Menu.vue";

export default {
  components: {
    Header,
    TwoColumns,
    Menu
  }
};
</script>
