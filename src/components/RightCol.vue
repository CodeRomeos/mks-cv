<template>
  <div class="right-col details">
    <br>
    <div class="about">
      <h2>
        <i class="fa fa-fw fa-info-circle"></i> ABOUT ME
      </h2>
      <p class="text" v-html="person.about"></p>
      <br>
      <p>
        <i class="fa fa-fw fa-calendar"></i>
        <strong>Date of Birth</strong>
        : {{ person.dob }}
      </p>
      <p class="location">
        <i class="fa fa-fw fa-map-marker"></i>
        <strong>Current Location:</strong>
        {{ person.location }}
      </p>
    </div>

    <employments/>
    <education/>
    <br>
    <projects/>
    <br>
    <hr>
    <br>
    <br>
    <app-footer/>
    <br>
    <br>
    <br>
    <br>
    <br>
    <br>
  </div>
</template>


<script>
import Employments from "./Employments";
import Education from "./Education";
import Projects from "./Projects";
import AppFooter from "./AppFooter";

export default {
  name: "RightCol",
  props: ["person"],
  data() {
    return {
      edit: null
    };
  },
  components: {
    Employments,
    Education,
    Projects,
    AppFooter
  }
};
</script>
