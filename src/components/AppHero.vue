<script>
export default {
  data() {
    return {
      img: new URL(`..\assets\jumbotron.jpg`, import.meta.url).href,
    };
  },
  mounted() {
    const myDiv = document.getElementById("jumbotron");
    myDiv.style.setProperty("--background-image", `url(${this.img})`);
  },
};
</script>

<template>
  <div class="container-fluid" id="jumbotron">
    <!-- <img :src="img" alt="jumbotron" /> -->
  </div>
</template>

<style>
#jumbotron {
  height: 200px;
  background-image: var(--background-image);
  background-repeat: repeat-x;
}
</style>
