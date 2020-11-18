<template>
  <div class="ultimate-features-wrapper">
    <div class="container-lg">
      <b-row class="d-flex align-items-center">
        <div class="col-md-7">
          <div class="left-ultimate">
            <div class="context-left">
              <h3>{{ txt.ultimateTitle }}</h3>
              <p class="my-3">{{ txt.ultimateSub }}</p>
            </div>

            <div class="main-list-ultimate">
              <div v-for="item in listUltimate" :key="item.id">
                <CateFeature
                  :image="item.img"
                  :title="item.title"
                  :description="item.description"
                  :container-style="{flexDirection:'column', alignItems:'left'}"
                  :img-style="{marginBottom:'2rem'}"
                  :content-style="{marginBottom: '1.5rem'}"
                />
              </div>
            </div>
            <b-button class="btn-try" pill variant="primary">See all</b-button>
          </div>
        </div>
        <div class="col-md-5">
          <div class="right-ultimate">
            <img alt="#" :src="images.phone3">
          </div>
        </div>
      </b-row>
    </div>
  </div>
</template>

<script>
import { Images } from '@/assets/Images'
import { listUltimate } from '@/static/shared/dummy'
import CateFeature from '@/components/card/CateFeature'

export default {
  name: 'UltimateFeatures',
  data() {
    return {
      images: {
        phone3: Images.phone3
      },
      txt: {
        ultimateTitle: 'Ultimate features that we built',
        ultimateSub: 'The rise of mobile devices transforms the way we consume information entirely.'
      },
      listUltimate: listUltimate
    }
  },
  components: {
    CateFeature
  }
}
</script>

<style lang="scss">
@use "static/base";

.ultimate-features-wrapper {
  background-image: url("../../../../assets/images/background-ulti.png");
  background-position: right center;
  background-repeat: no-repeat;
  background-size: initial;
}

.context-left {
  h3 {
    color: base.$primary-color;
    font-weight: bold;
    max-width: 320px;
  }

  p {
    color: base.$text-primary-color;
    max-width: 390px;
  }
}

.left-ultimate {
  @include base.columnLeft
}

.main-list-ultimate {
  @include base.listWrapBetween;
  margin-top: 2rem;
}

.right-ultimate {
  img {
    max-width: 100%;
  }
}
.btn-try {
  background-color: base.$btn-primary;
}
</style>
