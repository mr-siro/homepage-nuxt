<template>
  <div class="category-wrapper" :style="containerStyle">
    <div class="left-cate" :style="imgStyle">
      <img alt="#" :src="image">
    </div>
    <div class="right-cate" :style="contentStyle">
      <h5 :style="{color:titleColor, textAlign:textFloat}">{{ title }}</h5>
      <p :style="{textAlign: textFloat}">{{ description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CateFeature",
  props: {
    imgStyle: Object,
    textFloat: String,
    titleColor: String,
    image: String,
    title: String,
    contentStyle: Object,
    containerStyle: Object,
    description: String
  }
}
</script>

<style lang="scss">
@use "static/base";
.category-wrapper {
  display: flex;
}

.right-cate {
  p {
    max-width: 260px;
    color: base.$text-primary-color;
    text-align: left
  }

  h5 {
    font-weight: bold;
    text-align: left
  }
}
.left-cate {
  img {
    width: 85px;
    height: 85px;
  }
}
</style>
