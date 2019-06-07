<template>
  <nav>
    <v-toolbar flat app class="blue lighten-3">
      <v-toolbar-side-icon @click="toggleSidebar"></v-toolbar-side-icon>
      <v-toolbar-title>
        <span class="font-weight-light">Bob</span>
      </v-toolbar-title>
    </v-toolbar>

    <v-navigation-drawer v-model="drawer" app class="indigo">
      <p>Poop</p>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      showSidebar: false
    };
  },
  methods: {
    toggleSidebar() {
      this.showSidebar = !this.showSidebar;
    }
  }
};
</script>

<style>
</style>
