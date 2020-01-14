<template>
  <div class="menu">
    <div class="menu__lang">
      <button
        :ref="lang"
        v-for="lang in $i18n.availableLocales"
        :key="lang"
        class="menu__lang"
        @click="changeLocale(lang)"
        :disabled="lang === $i18n.locale ? true : false"
      >
        {{ lang }}
      </button>
    </div>
    <nav class="menu__nav" id="nav">
      <router-link class="menu__nav__link" to="/">{{
        $t("home.link")
      }}</router-link>
      |
      <router-link class="menu__nav__link" to="/about">{{
        $t("about.link")
      }}</router-link>
      |
      <router-link class="menu__nav__link" to="/gallery">{{
        $t("gallery.link")
      }}</router-link>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Menu",

  methods: {
    changeLocale(lang) {
      this.$i18n.locale = lang;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
