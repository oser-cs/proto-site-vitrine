<template>
<div class="navWide">
  <div class="links">
    <li v-for="link in links">
      <a :href="link.href">{{ link.text }}</a>
    </li>
  </div>
  <li class="login">
    <a href="#" class="login-button" type="button">
      <i class="fa fa-power-off"></i> Connexion
    </a>
  </li>
</div>
</template>

<script>
export default {
  name: 'NavWide',
  props: ['links']
}
</script>

<style lang="scss">
@import 'src/assets/scss/variables', 'src/assets/scss/mixins', 'src/assets/scss/media-queries';

.navWide {
    padding: 0;
    margin: $margin-page 0 0;
    list-style-type: none;
    display: none;
    flex: 1;

    .links {
        display: flex;

        li {
            @include nav-link($underline: true);
            margin-top: auto;
            // Add space between nav items
            & + li {
                margin-left: 16px;
            }
        }
    }
    // Login button
    li.login {
        margin: 0 0 auto auto;
    }
    a.login-button {
        @include btn($color-accent);
        @include btn-link;
    }
}
</style>
