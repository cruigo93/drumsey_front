<template>
  <div class="dashboard">
    <h1>Detect your sheet</h1>
    
    <input
      type="file"
      accept="image/*"
      @change="uploadImage($event)"
      id="file-input"
    />
    <br/>
    <img style="" :src="img_b64" alt="" width="720">
    
  </div>
</template>


<script>
import axios from "axios";
export default {
  components: {  },
  data() {
    return {
      list: [],
      img_b64: ''
    };
  },
  methods: {
    uploadImage(event) {
      const URL = "http://185.97.113.183:7890/predict";

      let data = new FormData();
      data.append("name", "my-picture");
      data.append("file", event.target.files[0]);

      let config = {
        header: {
          // "Content-Type": "image/png",
        },
      };

      axios.post(URL, data, config).then((response) => {
        // console.log("image upload response > ", response);
        this.img_b64 = response.data.base64
      });
    },
  },
};
</script>

<style>

</style>