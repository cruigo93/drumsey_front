<template>
  <div class="home">
    
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <div class="hello">
            <h1>DRUMSEY</h1>
            <p>make drum practice easy</p>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-md-4">
          <p class="headline_icon"><i class="fas fa-drum green"></i></p>
          <h3>METHODS</h3>
          <p>
            Stop wasting your practice time on random drum lessons. With an exclusive curriculum featuring the best teachers in the world, you’ll always know what to work on for maximum results.
          </p>
        </div>
        <div class="col-md-4">
          <p class="headline_icon"><i class="fas fa-headphones"></i></p>
          <h3>SONGS</h3>
          <p>
            Nothing is better than playing real music! You’ll love our songs area - including full transcriptions, audio loops, and practice tools for music by popular bands of all eras and styles.
          </p>
        </div>
        <div class="col-md-4">
          <p class="headline_icon"><i class="fas fa-school"></i></p>
          <h3>COACHES</h3>
          <p>
            Your favorite drummers have never been closer! You’ll get weekly live events and personal feedback with drum legends -- sharing their best advice and guiding your drumming journey.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    // HelloWorld,
  },
};
</script>

<style>
.home{
  margin: 15px;
}
.headline_icon{
  font-size: 8rem;
  
}
.headline_icon .green{
  color: "#ec0061"
}
</style>
