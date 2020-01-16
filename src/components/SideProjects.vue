<template>
  <div id="side-projects">
    <h1>side projects</h1>
    <p>I love programming, and I find the best way to learn is by doing. So here are my random projects.</p>
    <p>I'm experimenting with C++, Unreal Engine 4, iOS development, VueJS, Slackbots... and I've had the privilege of working on some of these projects with extremely talented people.</p>
    <p>
      These projects can be found on
      <a
        href="https://github.com/CheerfulSatchel"
        target="_blank"
      >my Github</a>.
    </p>
    <v-card>
      <v-container fluid grid-list-md>
        <v-layout row wrap>
          <v-flex
            v-for="item in items"
            :key="item.title"
            v-bind="{ [`sm${item.flex}`]: true }"
            class="card-flex"
          >
            <SideProjectsCard :cardDetails="item"/>
          </v-flex>
        </v-layout>
      </v-container>
    </v-card>
  </div>
</template>

<script>
import SideProjectsCard from "@/components/SideProjectsCard";

export default {
  data: () => ({
    items: [
      {
        title: "Star Runner 2019",
        description:
          "(2019-present)\n\nInfinite running game developed using Unreal Engine 4.\n\nMy friend and I wanted to learn Unreal Engine 4 and thought this would be a good starting point.\n\nWritten with C++11.",
        githubUrl: "https://github.com/theAmbientOrange/star-runner-2019",
        src:
          "https://raw.githubusercontent.com/theAmbientOrange/theAmbientOrange.github.io/development/src/assets/star-runner-2019-start-menu.png",
        flex: 6,
        showDescription: false
      },
      {
        title: "Blissbot",
        description:
          "(2019-present)\n\nA Slackbot that scrapes and fetches positive news articles from https://www.goodnewsnetwork.org/ and delivers them to your Slack workspace.\n\nWritten with Python 3.6.",
        githubUrl: "https://github.com/theAmbientOrange/blissbot",
        src:
          "https://raw.githubusercontent.com/theAmbientOrange/theAmbientOrange.github.io/development/src/assets/blissbot.png",
        flex: 6,
        showDescription: false
      },
      {
        title: "Miracle Messages",
        release: "https://apkpure.com/miracle-messages/com.miraclemessages",
        description:
          "(2016-2017)\n\nMy friends and I built this Android application for Miracle Messages, the non-profit organization reconnecting the homeless with their loved ones. I was the lead mobile developer, and we deployed the app onto the Google Play store back in October 2016.\n\nWritten with Java 8.",
        githubUrl: "https://github.com/miracle-messages/mm-android-mobile",
        src:
          "https://raw.githubusercontent.com/theAmbientOrange/theAmbientOrange.github.io/development/src/assets/miracle-messages.png",
        flex: 6,
        showDescription: false
      },
      {
        title: "Big Tuna",
        description:
          "(2018-present)\n\niOS app I am building with my friends that allows users to discover restaurants nearby via user posts and geolocation.\n\nWritten with Swift 5.",
        githubUrl: "https://github.com/aomori-nebuta/bigtuna-ios",
        src:
          "https://raw.githubusercontent.com/theAmbientOrange/theAmbientOrange.github.io/development/src/assets/bigtunalogoblue.png",
        flex: 6,
        showDescription: false
      }
    ]
  }),
  components: {
    SideProjectsCard
  }
};
</script>

<style>
</style>
