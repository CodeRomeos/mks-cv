<template>
  <div class="app-container">
    <left-col :person="person"></left-col>
    <right-col :person="person"></right-col>
  </div>
</template>

<script>
import LeftCol from "./components/LeftCol";
import RightCol from "./components/RightCol";

export default {
  name: "App",
  data() {
    return {
      person: {
        name: "Mukesh Kumar",
        position: "Front-End Developer",
        about:
          "Courteous and enthusiastic, I am interested in IT and everything in its orbit. I am keen to gain more experience in the field of Web Design and developement. I would offer my full commitment, and be a pleasant and friendly addition to the team. <br>Able to effectively self-manage during independent projects, as well as collaborate in a team setting. Write about design & development <strong>@CodeRomeos</strong>.",
        dob: "05th Dec, 1991",
        location: "New Delhi",
        skills: [
          "HTML5",
          "CSS3",
          "CSS Grid System",
          "CSS Pre-processors - Sass/SCSS",
          "Bootstrap",
          "Responsive Web Design",
          "JavaScript(Basic)",
          "WordPress"
        ],
        phone: "+91-880 220 0997",
        email: "kashyapmukesh91@gmail.com",
        github: "github.com/mukesh-kashyap",
        twitter: "twitter.com/001abid",
        address: "RZ-C-103, Nihal Vihar, Nangloi, New Delhi 110041",
        hobbies: [
          "Listening to Music",
          "Playing Cricket",
          "Reading Books and Novels",
          "Watching Movies"
        ],
        versioningTools: "Git",
        versioningSystems: ["GitHub", "Bitbucket"]
      }
    };
  },
  components: {
    LeftCol,
    RightCol
  }
};
</script>

<style lang="scss">
@import "./assets/main.scss";
</style>
