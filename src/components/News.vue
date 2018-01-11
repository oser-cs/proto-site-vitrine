<template lang="html">
<div id="news">
  <div class="heading">
    <h2>L'actualité de l'association</h2>
    <div class="link-all">
      <a href="#" type="button">Tous les articles</a>
    </div>
  </div>
  <ul class="news-cards">
    <NewsCard v-for="card in cards"
      :key="card.key"
      :title="card.title"
      :description="card.description"
      :date="card.date"
      :src="card.src"/>
  </ul>
</div>
</template>

<script>
import NewsCard from './NewsCard'

export default {
  name: 'News',
  components: {
    NewsCard
  },
  data: function () {
    return {
      cards: [{
          key: 1,
          title: 'Journée de Clôture 2017',
          description: "La fin de l'année scolaire sonne aussi la fin du tutorat pour les tutorés. Pour fêter cette belle année passée ensemble, les tutorés et les tuteurs se sont retrouvés ce samedi 5 juin sur le campus de CentraleSupélec […]",
          date: '15/06/17',
          src: require('../assets/img/news-jdc.jpg')
        },
        {
          key: 2,
          title: 'Retour sur Focus Europe 2017',
          description: "Il est l'heure de faire le bilan de cette édition 2017 de Focus Europe, qui a emmené les tutorés à Prague. L'équipe organisatrice vous a préparé une belle brochette de photos ainsi qu'un montage souvenir […]",
          date: '30/04/17',
          src: require('../assets/img/news-focus-bilan.jpg')
        },
        {
          key: 3,
          title: "Focus Europe 2017 : c'est parti !",
          description: "Les lycéens sont arrivés ce jeudi 13 avril à Prague, capitale de la République Tchèque. Au programme : découverte de la ville, visites culturelles, jeu de piste, et surtout beaucoup de bonne humeur ! […]",
          date: '03/04/17',
          src: require('../assets/img/news-focus-c-est-parti.jpg')
        }
      ]
    }
  }
}
</script>

<style lang="scss">
@import 'src/assets/scss/variables', 'src/assets/scss/mixins', 'src/assets/scss/media-queries';
#news {
    @include landing-section(3);
    .heading {
        text-align: center;
        // margin-bottom: 3em;
    }
    .link-all {
        text-align: center;
        margin: 0;
        a {
            @include btn($color-dark-blue);
            @include btn-link;
        }
    }
    .news-cards {
        display: flex;
        flex-direction: column;
        justify-content: center;
        padding: 0;
        list-style-type: none;
        margin: 2em 0;
        @include media-md() {
            flex-direction: row;
        }
    }
}
</style>
