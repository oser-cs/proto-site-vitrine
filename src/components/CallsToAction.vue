<template>
<div id="calls-to-action">
  <div class="heading">
    <h2>Ensemble, osons agir.</h2>
  </div>
  <div class="cta">
    <div class="cta-text">
      <p>
        Ils nous soutiennent cette année encore : <strong>merci à nos partenaires pour leur engagement !</strong>
      </p>
      <p>
        Vous aussi, engagez-vous à nos côtés en devenant <strong>partenaire d'Ouverture Sociale pour l'Égalité et la Réussite</strong>.
      </p>
      <Button title="Devenir partenaire" color="rgb(213, 250, 255)" hoverColor="rgb(46, 37, 128)"/>
    </div>
    <div class="cta-well white">
      <img src="~assets/img/partenaires-akoya.png" alt="Akoya Consulting">
      <img src="~assets/img/partenaires-safran.png" alt="Safran">
    </div>
  </div>
  <div class="cta">
    <div class="cta-text">
      <p>
        OSER fait partie de la Cordée Mutualisée de l'Université Paris Saclay, projet visant à favoriser l'accès à l'enseignement supérieur, dont les  lières d'excellence, de jeunes quel que soit leur milieu socioculturel. Notre action est ainsi en partie financée par des organismes régionaux et départementaux.
      </p>
      <p>
        Vous aussi, <strong>soutenez notre action auprès des jeunes de la région parisienne</strong>.
      </p>
      <Button title="Faire un don" color="rgb(213, 250, 255)" hoverColor="rgb(46, 37, 128)"/>
    </div>
    <div class="cta-well">
      <img src="~assets/img/partenaires-cget.png" alt="CGET">
      <img src="~assets/img/partenaires-rectorat.png" alt="Rectorat">
      <img src="~assets/img/partenaires-ridf.png" alt="RIDF">
      <img src="~assets/img/partenaires-upsaclay.png" alt="UPSaclay">
    </div>
  </div>
</div>
</template>

<script>
import Button from "./Button"

export default {
  name: "CallsToAction",
  components: {Button}
}
</script>

<style lang="scss">
@import 'src/assets/scss/variables', 'src/assets/scss/mixins', 'src/assets/scss/media-queries';

#calls-to-action {
  @include landing-section(4);
  background-color: $color-dark-blue;
  color: white;

  .heading {
    text-align: center;
  }

  h2 {
    color: $color-light-blue;
  }

  .cta {
    display: grid;
    grid-template-areas: "text well";
    grid-gap: 2em;
    margin-bottom: 2em;
    .btn {
      margin-top: 2em;
    }
  }

  .cta-text {
    grid-area: "text";
  }

  .cta-well {
    grid-area: "well";
    width: 30em;
    margin-bottom: auto;
    text-align: center;
    box-shadow: 0 3px 10px 3px rgba(0, 0, 0, 0.2) inset;
    border-radius: 4px;
    img {
      vertical-align: middle;
      max-width: 49%;
      height: auto;
    }
    &.white {
      background: white;
    }
  }
}
</style>
