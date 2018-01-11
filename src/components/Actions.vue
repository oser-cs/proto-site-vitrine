<template lang="html">
  <div id="axes-action">
    <h2>{{ title }}</h2>
    <ul class="actions">
      <div class="action-bubble" v-for="action in actions" :key="action.key">
        <img :src="action.src" :alt="action.title">
        <p>{{ action.title }}</p>
      </div>
    </ul>
    <p>{{ summary }}</p>
    <a type="button" href="#">{{ cta }}</a>
  </div>
</template>

<script>
export default {
  name: 'Actions',
  data: function () {
    return {
      title: "Nous agissons pour plus d'égalité des chances",
      summary: 'De la seconde à la Terminale, nous sommes présents sur tous les fronts pour accompagner le développement de nos lycéens.',
      cta: 'En savoir plus',
      actions: [
        {
          key: 1,
          title: 'Apprendre, comprendre',
          src: require('../assets/img/action-apprendre.jpg')
        },
        {
          key: 2,
          title: "Découvrir, s'intéresser",
          src: require('../assets/img/action-decouvrir.jpg')
        },
        {
          key: 3,
          title: "Vivre l'extraordinaire",
          src: require('../assets/img/action-vivre.jpg')
        }
      ]
    }
  }
}
</script>

<style lang="scss">
@import 'src/assets/scss/variables', 'src/assets/scss/mixins';

#axes-action {
    @include landing-section(2);
    background: $color-light-blue;
    text-align: center;

    a {
        @include btn($color-accent);
        @include btn-link;
    }

    .actions {
        display: flex;
        justify-content: center;
        padding: 0;
        list-style-type: none;
    }

    p {
        margin-bottom: 2em;
    }
}
.action-bubble {
  text-align: center;

  img {
    width: 100%;
    max-width: 200px;
    height: auto;
    border-radius: 50%;
  }

  p {
    text-transform: uppercase;
    font-weight: bold;
    color: $color-dark-blue;
  }

  & + .action-bubble {
    margin-left: 3em;
  }
}
</style>
