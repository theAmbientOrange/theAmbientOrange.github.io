<template>
  <nav>
    <v-toolbar flat app class="blue lighten-3">
      <v-toolbar-side-icon @click="toggleSidebar"></v-toolbar-side-icon>
      <v-spacer></v-spacer>
      <v-toolbar-title>
        <span class="font-weight-light">theAmbientOrange 🍊</span>
      </v-toolbar-title>
    </v-toolbar>

    <v-navigation-drawer v-model="showSidebar" width="225" app class="blue lighten-3">
      <v-list three-line class="pt-50">
        <v-list-tile v-for="item in items" :key="item.text" @click="handleOnClick(item)">
          <v-list-tile-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>

          <v-list-tile-content>
            <v-list-tile-title>{{ item.text }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      showSidebar: false,
      items: [
        { icon: "account_circle", text: "about", to: "about" },
        { icon: "work", text: "career", to: "career" },
        { icon: "code", text: "side projects", to: "side-projects" },
        { icon: "chat", text: "contact", to: "contact" }
      ]
    };
  },
  methods: {
    toggleSidebar() {
      this.showSidebar = !this.showSidebar;
    },
    handleOnClick(item) {
      const element = document.getElementById(item.to);
      console.log(element);
      element.scrollIntoView();
    }
  }
};
</script>

<style>
</style>