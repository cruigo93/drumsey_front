<script>
export default {
  props: {
    name: { type: String, required: true },
    desc: { type: String, required: true },
    price: { type: Number, required: true },
    rating: { type: Number, required: true },
  },
  methods: {},
  created(){
    console.log('Name: ',name)
  }
};
</script>

<template>
  <!-- <div>
        <h3>{{ name }}</h3>
    </div> -->

 <div class="card" style="width: 18rem; height: 24rem">
  <div class="card-body">
    <h3><i class="fas fa-drum"></i></h3>
    <h5 class="card-title">{{ name }}</h5>
    <p class="card-text">{{ desc }}</p>
    <a href="#" class="btn btn-success">Practice</a>
  </div>
  <div class="card-footer text-muted">
    Price: {{ price }} KZT
  </div>
</div>
</template>