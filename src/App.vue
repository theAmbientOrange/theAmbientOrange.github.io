<template>
  <v-app>
    <NavigationBar/>
    <v-content></v-content>
  </v-app>
</template>

<script>
import NavigationBar from "@/components/NavigationBar";

export default {
  name: "App",
  components: {
    NavigationBar
  },
  data() {
    return {
      //
    };
  }
};
</script>
