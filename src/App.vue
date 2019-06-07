<template>
  <v-app>
    <Sidebar/>
    <v-content>
      <Content id="content"/>
    </v-content>
  </v-app>
</template>

<script>
import Sidebar from "@/components/Sidebar";
import Content from "@/components/Content";

export default {
  name: "App",
  components: {
    Sidebar,
    Content
  },
  data() {
    return {
      //
    };
  }
};
</script>

<style>
#content {
  position: fixed;
  margin-left: 10%;
  margin-right: 10%;
  margin-top: 10%;
}
</style>
