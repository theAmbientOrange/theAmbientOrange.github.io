<template>
  <div id="content">
    <div id="about">
      <h1>about</h1>
      <p>Hello! My name is James Wu, and thank you for visiting my website.</p>
      <p>I received my Bachelor of Science degree in Computer Science from the University of Virginia.</p>
      <p>My interests lie largely in developing real-time systems, writing C++ code, and video game development.</p>
      <p>I am currently a software engineer in Small Business Card Tech at Capital One.</p>
      <p>Outside of work, I love making and playing video games, making 3D models, running marathons, hiking, and watching MIT OpenCourseware videos.</p>
    </div>
    <div id="career">
      <h1>career</h1>
      <v-timeline align-top>
        <v-timeline-item v-for="(item, i) in items" :key="i" :color="item.color" :icon="item.icon">
          <template v-slot:opposite>
            <span :class="`headline font-weight-bold ${item.color}--text`" v-text="item.dates"></span>
          </template>
          <div class="py-3">
            <h2 :class="`headline font-weight-light mb-3 ${item.color}--text`">{{item.title}}</h2>
            <div>{{item.description}}</div>
          </div>
        </v-timeline-item>
      </v-timeline>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        color: "blue",
        icon: "work",
        title: "software engineer @ Capital One",
        dates: "February 2018 - present",
        description:
          "Transaction Underwriting and Deployment Pipeline Compliance (Java, Python)"
      },
      {
        color: "orange",
        icon: "school",
        title: "graduated from University of Virginia",
        dates: "December 2017",
        description: "finished undergraduate studies with high honors"
      },
      {
        color: "blue",
        icon: "star_border",
        title: "intern @ Capital One",
        dates: "Summer 2017",
        description:
          "developed Apache Spark application for Rewards Earn Engine (Java)"
      },
      {
        color: "purple",
        icon: "star_border",
        title: "intern @ Leidos",
        dates: "Summer 2016",
        description:
          "contributed to RDUCE, a LIDAR compression application (C++)"
      },
      {
        color: "blue",
        icon: "star_border",
        title: "intern @ Fairfax Collegiate",
        dates: "Summer 2015",
        description: "taught (rowdy) 4-8th grade students Lego Mindstorms"
      },
      {
        color: "orange",
        icon: "school",
        title: "started school @ University of Virginia",
        dates: "August 2014",
        description: "began undergraduate studies in engineering"
      }
    ]
  })
};
</script>

<style>
/*Based on https://stackoverflow.com/a/38994837*/
#content {
  overflow-y: auto;
  -ms-overflow-style: none; /*IE 10+*/
  scrollbar-width: none; /*Firefox*/
}

#content::-webkit-scrollbar {
  display: none; /*Safari and Chrome*/
}

h1 {
  padding-top: 20px;
  padding-bottom: 20px;
}
</style>
