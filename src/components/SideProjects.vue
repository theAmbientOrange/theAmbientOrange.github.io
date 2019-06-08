<template>
  <div id="side-projects">
    <h1>side projects</h1>
    <p>I love programming, and I find the best way to learn is by doing. So here are my random projects.</p>
    <p>I'm experimenting with C++, Unreal Engine 4, iOS development, VueJS, Slackbots... and I've had the privilege of working on some of these with extremely talented people.</p>
    <p>
      These projects can be found on
      <a
        href="https://github.com/theAmbientOrange"
        target="_blank"
      >my Github</a>.
    </p>
    <v-card>
      <v-container fluid grid-list-md>
        <v-layout row wrap>
          <v-flex v-for="item in items" :key="item.title" v-bind="{ [`xs${item.flex}`]: true }">
            <v-card id="side-project-card">
              <v-img :src="item.src" height="80%">
                <v-container fill-height fluid pa-2>
                  <v-layout fill-height></v-layout>
                </v-container>
              </v-img>
              <v-card-actions>
                {{item.title}}
                <v-spacer></v-spacer>
                <v-btn icon :href="item.githubUrl" target="_blank">
                  <img src="../assets/github-circle.svg">
                </v-btn>
                <v-btn icon>
                  <v-icon color="pink">description</v-icon>
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>
    </v-card>
  </div>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        title: "Big Tuna",
        description: "yo",
        githubUrl: "https://github.com/aomori-nebuta/bigtuna-ios",
        src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
        flex: 6
      }
    ]
  })
};
</script>

<style>
#side-project-card {
  border-radius: 30px;
}
</style>
