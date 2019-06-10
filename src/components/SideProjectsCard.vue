<template>
  <v-card class="card-flex">
    <v-container class="card-container">
      <div class="upper-card-container">
        <img class="card-image" v-if="!cardDetails.showDescription" :src="cardDetails.src">
        <v-textarea
          class="card-description"
          v-else
          rows="10"
          :value="cardDetails.description"
          readonly
          outline
        ></v-textarea>
      </div>
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
      cardDetails.showDescription = !cardDetails.showDescription;
    }
  }
};
</script>

<style>
.card-container {
  overflow: hidden;
  position: relative;
  height: 50vw;
  width: 100%;
}

.card-image {
  object-fit: contain;
  overflow: hidden;
}

.upper-card-container {
  height: 100%;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.card-flex {
  border-radius: 30px;
}

/* .card-description {
  height: 100%;
} */
</style>
