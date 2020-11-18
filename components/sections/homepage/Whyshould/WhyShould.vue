<template>
  <div class="why-should-wrapper">
    <b-container>
      <div class="main-text-why">
        <h3>{{txt.whyTitle}}</h3>
        <p>{{txt.whySub}}</p>
      </div>
      <div class="main-list-why">
        <div v-for="item in listWhy" :key="item.id">
          <CateFeature
          :image="item.img"
          :title="item.title"
          :description="item.description"
          :container-style="{flexDirection:'column', alignItems:'center'}"
          :text-float="'center'"
          :img-style="{marginBottom:'2rem'}"
          :content-style="{marginBottom: '3rem'}"
          />
        </div>
      </div>
    </b-container>
  </div>
</template>

<script>
import {listWhy} from "@/static/shared/dummy";
import CateFeature from "@/components/card/CateFeature";
export default {
  name: "WhyShould",
  data() {
    return {
      txt: {
        whyTitle: 'Why you should choose our app',
        whySub: "The rise of mobile devices transforms the way we consume information entirely and the world's most elevant channels such as Facebook."
      },
      listWhy:listWhy
    }
  },
  components:{
    CateFeature
  }
}
</script>

<style lang="scss">
@use "static/base";
.why-should-wrapper {
  padding-top: 6rem;
  display: flex;
  justify-content: center;
  align-items: center;
}

.main-text-why {
  max-width: 640px;
  display: inline-block;

  h3 {
    color: base.$primary-color;
    font-weight: bold;
  }
  p {
    text-align: center;
    color: base.$text-primary-color;
  }
}

.main-list-why {
  @include base.listWrapBetween;
  margin: 5rem;
  align-items: center;
}

</style>
