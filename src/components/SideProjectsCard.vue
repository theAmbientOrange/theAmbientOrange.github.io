<template>
  <v-card id="side-project-card">
    <v-container class="paul">
      <v-layout align-center justify-center>
        <img class="side-project-image" v-if="!cardDetails.showDescription" :src="cardDetails.src">
        <!-- <v-container fill-height fluid pa-2>
                  <v-layout fill-height></v-layout>
        </v-container>-->
        <v-textarea
          v-else
          class="align-center justify-center fill-height text-xs-center pa-1"
          id="guy"
          disabled
          solo
          outline
          value="yo"
        ></v-textarea>
      </v-layout>
    </v-container>

    <v-card-actions>
      {{cardDetails.title}}
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon color="pink" @click="handleOnDescriptionClick(cardDetails)">description</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon color="green">important_devices</v-icon>
      </v-btn>
      <v-btn icon :href="cardDetails.githubUrl" target="_blank">
        <img src="../assets/github-circle.svg">
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  props: {
    cardDetails: {
      type: Object,
      default: () => {}
    }
  },
  methods: {
    handleOnDescriptionClick(cardDetails) {
      console.log("YEEEEAAAH " + cardDetails.showDescription);
      cardDetails.showDescription = !cardDetails.showDescription;
    }
  }
};
</script>

<style>
</style>
