<template lang="html">
  <div>
    <img id="landing-photo" src="~assets/img/groupe.jpg" alt="Photo de groupe">
    <QuiSommesNous/>
    <Actions/>
    <News/>
  </div>
</template>

<script>
import QuiSommesNous from './QuiSommesNous'
import Actions from './Actions'
import News from './News'

export default {
  name: 'LandingPage',
  components: {
    QuiSommesNous,
    Actions,
    News
  }
}
</script>

<style lang="scss">
@import 'src/assets/scss/mixins';
#landing-photo {
    position: relative;
    z-index: -1;  // make shadow of navbar cover the photo
    display: block;
    width: 100%;
    height: auto;
    margin: 0;
    @extend %shadow;
}
</style>
