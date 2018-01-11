<template>
<div class="navNarrow">
  <i v-on:click="toggle" class="fa fa-bars fa-2x"></i>
  <div v-show="visible" class="links">
    <li v-for="link in links">
      <a :href="link.href">{{ link.text }}</a>
    </li>
    <li>
      <a href="#">
        <i class="fa fa-power-off"></i> Connexion</a>
    </li>
  </div>
</div>
</template>

<script>
export default {
  name: 'NavNarrow',
  props: ['links'],
  data: function () {
    return {
      visible: false
    }
  },
  methods: {
    toggle: function (event) {
      this.visible = !this.visible
    }
  }
}
</script>

<style lang="scss">
@import 'src/assets/scss/variables', 'src/assets/scss/mixins';

.navNarrow {
    display: flex;
    padding: 0;
    margin: $margin-page 0;
    list-style-type: none;
    flex-direction: column;
    flex: 1;

    i {
        cursor: pointer;
        margin-left: auto;
        margin-right: 0;
        color: $color-dark-blue;
    }

    .links {
        padding-top: 20px;
        max-height: 100%;
        transition: max-height 0.3s;
        overflow: hidden;
        li {
            @include nav-link;
            text-align: right;
            margin-left: auto;
            margin-right: 0;

            & + li {
                margin-top: 16px;
            }
        }
    }
}
</style>
