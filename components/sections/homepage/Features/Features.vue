<template>
  <div class="features-wrapper">
    <b-row class="d-flex align-items-center">
      <div class="col-md-6">
        <div class="left-ft">
          <img  alt="#" :src="images.phone2">
        </div>
      </div>
      <div class="col-md-6">
        <div class="right-ft">
          <h3 class="ft-title">{{ txt.title }}</h3>
          <p class="ft-sub">{{ txt.subTitle }}</p>
          <div v-for="item in listCate" :key="item.id">
            <CateFeature
                :container-style="{flexDirection:'row', alignItems:'center'}"
                :contentStyle="{marginLeft:'1.5rem'}"
                class="pt-4" :image="item.img"
                :title="item.title"
                :description="item.description"
                :title-color="item.color"/>
          </div>
        </div>
      </div>
    </b-row>
  </div>
</template>

<script>
import {Images} from "@/assets/Images";
import CateFeature from "@/components/card/CateFeature";
import {listCate} from "@/static/shared/dummy";

export default {
  name: "Features",
  data() {
    return {
      images: {
        phone2: Images.phone2
      },
      txt: {
        title: 'Awesome apps features',
        subTitle: 'Increase productivity with a simple to-do app. app for managing your personal budgets.'
      },
      listCate: listCate
    }
  },
  components: {
    CateFeature
  }
}
</script>

<style lang="scss">
@use "static/base";
.features-wrapper {
  margin: 0 1rem;
}

.right-ft {
  @include base.columnLeft
}
.left-ft {
  img {
    max-width: 100%;
  }
}
.ft-title {
  color: base.$primary-color;
  font-weight: bold;
  max-width: 280px;
}

.ft-sub {
  color: base.$text-primary-color;
  max-width: 430px;
}
</style>
