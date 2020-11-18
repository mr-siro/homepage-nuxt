<template>
  <div class="designed-wrapper">
    <b-row class="d-flex align-items-center">
      <div class="col-md-6">
        <div class="left-design">
          <img  alt="#" :src="images.imgDesign">
        </div>

      </div>
      <div class="col-md-6">
        <div class="right-design">
          <h3 class="ds-title">{{txt.designTitle}}</h3>
          <p class="ds-sub my-4">{{txt.designDes}}</p>
          <b-button class="btn-try" pill variant="primary">Learn more</b-button>
        </div>
      </div>
    </b-row>
  </div>
</template>

<script>
import {Images} from "@/assets/Images";

export default {
  name: "Designed",
  data() {
    return {
      images: {
        imgDesign: Images.DesignImg
      },
      txt: {
        designTitle: 'Designed & built by the latest code integration',
        designDes: "The rise of mobile devices transforms the way we consume information entirely and the world's most elevant channels such as Facebook."
      }
    }
  }
}
</script>

<style lang="scss">
@use "static/base";
.designed-wrapper {
  margin: 0 2em;
}

.left-design {
  img {
    max-width: 100%;
  }
}
.right-design {
  @include base.columnLeft
}
.ds-title {
  color: base.$primary-color;
  font-weight: bold;
  max-width: 360px;
}
.ds-sub {
  color: base.$text-primary-color;
  max-width: 400px;
}

.btn-try {
  background-color: base.$btn-primary;
}
</style>
