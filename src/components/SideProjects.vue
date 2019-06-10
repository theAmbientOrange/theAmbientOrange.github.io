<template>
  <div id="side-projects">
    <h1>side projects</h1>
    <p>I love programming, and I find the best way to learn is by doing. So here are my random projects.</p>
    <p>I'm experimenting with C++, Unreal Engine 4, iOS development, VueJS, Slackbots... and I've had the privilege of working on some of these projects with extremely talented people.</p>
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
          <v-flex
            v-for="item in items"
            :key="item.title"
            v-bind="{ [`sm${item.flex}`]: true }"
            id="yee"
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
        title: "Miracle Messages",
        description: "Greetings boi",
        githubUrl: "https://github.com/miracle-messages/mm-android-mobile",
        src:
          "https://images.unsplash.com/photo-1534448177492-6d698f12a59a?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1000&q=80",
        flex: 6,
        showDescription: false
      },
      {
        title: "Big Tuna",
        description: "Greetings boi",
        githubUrl: "https://github.com/miracle-messages/mm-android-mobile",
        src:
          "https://raw.githubusercontent.com/theAmbientOrange/theAmbientOrange.github.io/master/src/assets/miracle-messages.png",
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
#paul {
  width: 100%;
  height: 50vw;
  position: relative;
}

#guy {
  height: 100%;
  border: none;
  position: absolute;
  bottom: 0px;
}
.side-project-image {
  width: 50vw;
  height: 50vw;
  object-fit: contain;
  overflow: hidden;
}
#side-project-card {
  border-radius: 30px;
}
</style>
