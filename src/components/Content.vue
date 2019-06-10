<template>
  <div id="content">
    <div id="about">
      <h1>about</h1>
      <img id="picture-of-me" src="../assets/james.jpg">
      <p>Hello! My name is James Wu, and thank you for visiting my website.</p>
      <p>My primary interests are in video game development, writing C++ code, and real-time systems.</p>
      <p>I received my Bachelor of Science degree in Computer Science from the University of Virginia.</p>
      <p>I am proficient with C/C++, Java, and Python. I am familiar with Swift and Javascript.</p>
      <p>I am currently a software engineer in Small Business Card Tech at Capital One.</p>
      <p>Outside of work, I love making video games using Unreal Engine 4, attempting to make 3D models using Blender, running marathons, hiking, playing video games, and watching MIT OpenCourseware videos.</p>
    </div>
    <Career/>
    <SideProjects/>
    <div id="contact">
      <h1>contact</h1>
      <p>
        <v-icon>phone</v-icon>703-439-7279
      </p>
      <p>
        <v-icon>email</v-icon>therealjameswu@gmail.com
      </p>
    </div>
  </div>
</template>

<script>
import Career from "@/components/Career";
import SideProjects from "@/components/SideProjects";

export default {
  components: {
    Career,
    SideProjects
  }
};
</script>

<style>
/*Based on https://stackoverflow.com/a/38994837*/
#content {
  width: 80%;
  overflow-y: auto;
  -ms-overflow-style: none; /*IE 10+*/
  scrollbar-width: none; /*Firefox*/
}

#content::-webkit-scrollbar {
  display: none; /*Safari and Chrome*/
}

#picture-of-me {
  float: right;
  width: 25%;
  height: 25%;
  border-radius: 30px;
}

h1 {
  padding-top: 20px;
  padding-bottom: 20px;
}
</style>
