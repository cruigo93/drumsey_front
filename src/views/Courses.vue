<script>
import Course from "@/components/course/Course";
import axios from "axios";
export default {
  components: { Course },
  data() {
    return {
      list: [],
    };
  },
  created() {
    axios
      .get("http://localhost:8800/course", {
        headers: {
          // remove headers
        },
      })
      .then((response) => {
        console.log(response.data);
        this.list = response.data.list;
      })
      .catch((error) => {
        this.errorMessage = error.message;
        console.error("There was an error!", error);
      });
  },
};
</script>

<template>
  <div class="courses">
    <h1>Study Drums with Ease</h1>
    <h3>Choose study plan</h3>
    <!-- <Course name="Course1" price="390" rating="48" />
    -->

    <div class="container">
      <div class="row">
        <div class="col-md-3" v-for="(course, index) of list" :key="index">
          <Course
            v-bind:name="course.name"
            v-bind:price="course.price"
            v-bind:rating="course.rating"
            v-bind:desc="course.desc"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.courses {
  margin: 15px;
}
</style>