<template>
<div class='navbar'>
  <div class='logo-container'>
    <img src='~assets/img/oser-logo-slogan.png' alt='Logo' class='logo'>
  </div>
  <NavWide :links='links' />
  <NavNarrow :links='links' />
</div>
</template>

<script>
import NavWide from './NavWide'
import NavNarrow from './NavNarrow'

export default {
  name: 'Navbar',
  data() {
    return {
      links: [{
        href: '#',
        text: 'Qui sommes-nous ?'
      }, {
        href: '#',
        text: 'Soutenez-nous'
      }, {
        href: '#',
        text: 'Nos actions'
      }, {
        href: '#',
        text: 'Actualités'
      }, {
        href: '#',
        text: 'Contact'
      }]
    }
  },
  components: {
    NavWide,
    NavNarrow
  }
}
</script>

<style lang='scss'>
@import 'src/assets/scss/variables', 'src/assets/scss/mixins', 'src/assets/scss/media-queries';
.navbar {
    position: static;
    top: 0;
    display: flex;
    flex-direction: row;
    padding: 0 $margin-page;
    margin: 0;
    background: white;
    @extend %shadow;

    .logo-container {
        padding: $col-padding;
        margin: 0 auto;

        img.logo {
            width: 100%;
            max-width: 15em;
        }
    }
}
@include media-md() {
    .navbar {
        .logo-container {
            width: col-width(3);
        }

        .navWide {
            display: flex;
        }

        .navNarrow {
            display: none;
        }
    }
}
</style>
