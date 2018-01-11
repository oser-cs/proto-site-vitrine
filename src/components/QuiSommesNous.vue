<template lang="html">
  <div id="qui-sommes-nous">
    <h2>Qui sommes-nous ?</h2>
    <p>
      <strong>Ouverture Sociale pour l'Égalité et la Réussite</strong> est une association loi 1901 composée d'étudiants et d'étudiantes de CentraleSupélec engagés pour plus d'égalité des chances face aux études supérieures.
      <br><br>
      Nous souhaitons que <strong>chacun, quelles que soient ses origines sociales, économiques ou culturelles, puisse forger son avenir et se munir des clés pour réaliser ses ambitions</strong>.
    </p>
    <div class="next">
      <a type="button" href="#">Lire la suite</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'QuiSommesNous'
}
</script>

<style lang="scss">
@import 'src/assets/scss/variables', 'src/assets/scss/mixins';
#qui-sommes-nous {
    @include landing-section(1, white);
    background: $color-dark-blue;
    text-align: center;

    h2 {
        color: $color-light-blue;
    }

    p {
        margin-bottom: 2em;
    }
    .next {
        margin-bottom: 2em;
    }
    a {
        @include btn(white, $hover-color: $color-dark-blue);
        @include btn-link;
    }
}
</style>
