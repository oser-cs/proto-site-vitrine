<template>
  <div id="footer">
    <div class="inline-text">
      Newsletter : recevez toute notre actualité
      <Button
      title="M'inscrire"
      color="rgb(151, 146, 192)"
      hoverColor="rgb(32, 26, 78)"/>
    </div>
    <div class="inline-text">
      Contact | Mentions légales &amp; crédits
    </div>
    <div class="inline-text">
      <i class="social fa fa-2x fa-facebook"></i>
      <i class="social fa fa-2x fa-twitter"></i>
    </div>
  </div>
</template>

<script>
import Button from "./Button";

export default {
  name: "Footer",
  components: {Button}
}
</script>

<style lang="scss">
@import 'src/assets/scss/variables', 'src/assets/scss/mixins', 'src/assets/scss/media-queries';

#footer {
  position: relative;
  z-index: 30;
  background: $color-darkest-blue;
  padding: $margin-page 3*$margin-page;
  color: $color-purple-light;
  display: flex;
  justify-content: space-between;
}
.inline-text {
  .btn {
    display: inline;
    vertical-align: baseline;
    margin-left: 1em;
  }
  .social {
    margin: 0 0.5em;
    color: $color-light-blue;
  }
}

</style>
