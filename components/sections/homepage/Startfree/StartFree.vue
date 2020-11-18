<template>
<div class="start-free-wrapper">
  <b-container>
    <div class="main-start">
      <h2>Download our App now !</h2>
      <p class="py-2">{{txt.sub}}</p>
      <div class="view-download">
        <img class="mx-2" alt="#" :src="images.chPlay">
        <img class="ml-2" alt="#" :src="images.appStore">
      </div>
    </div>
  </b-container>
</div>
</template>

<script>
import {Images} from "@/assets/Images";

export default {
name: "StartFree",
  data() {
  return {
    txt:{
      sub:"The rise of mobile devices transforms the way we consume information entirely and the world's most elevant channels such as Facebook."
    },
    images:{
      chPlay: Images.chPlay,
      appStore: Images.appStore
    }
  }
  }
}
</script>

<style lang="scss">
@use "static/base";
.start-free-wrapper {
  background-image: url("../../../../assets/images/bg_start_03.png");
  background-position: right bottom;
  background-repeat: no-repeat;
  background-size: initial;
  padding-top: 10%;
  border-top: base.$base-border;
  min-height: 380px;
  h2 {
    color: base.$primary-color;
    font-weight: bold;
    text-align: left;
  }
  p {
    color: base.$text-primary-color;
    text-align: left;
  }
}



.main-start {
  @include base.columnLeft;
  max-width: 600px;
}
.view-download {
  img {
    max-width: 120px;
  }
}
</style>
