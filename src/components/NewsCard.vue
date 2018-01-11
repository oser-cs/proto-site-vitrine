<template lang="html">
<div class="news-card">
  <div class="img">
    <img :src="src" :alt="title"/>
  </div>
  <div class="body">
    <h3>{{ title }}</h3>
    <h5>Publié le {{ date }}</h5>
    <p>{{ description }}</p>
    <a href="#">Lire la suite</a>
  </div>
</div>
</template>

<script>
export default {
  name: 'NewsCard',
  props: ['src', 'title', 'description', 'date']
}
</script>

<style lang="scss">
@import 'src/assets/scss/variables', 'src/assets/scss/mixins', 'src/assets/scss/media-queries';

.news-card {
    $padding: 1em 1.5em;
    display: flex;
    min-height: 100%;
    margin: 0;
    padding: 0;
    @include media-md {
        background-color: #f6f6f6;
        border-radius: 0.5em;
        overflow: hidden;
        display: block;
        max-width: 20em;
    }
    .img {
        display: none;
        margin-bottom: auto;
        margin-right: 2em;
        @include media-xs {
            display: block;
        }
        @include media-md {
            margin: 0;
        }
    }
    img {
        width: 10em;
        height: auto;
        border-radius: 0.5em;
        overflow: hidden;
        @include media-md {
            width: 100%;
            border-radius: 0;
        }
    }
    .body {
        @include media-md {
            padding: $padding;
        }
        h3 {
            font-family: $font-title;
            font-weight: bold;
            margin: 0;
        }
        h5 {
            color: gray;
            font-weight: normal;
            margin: 0;
            padding: 0;
        }
        a {
            text-decoration: none;
            color: $color-accent;
            font-weight: bold;
        }
    }
    & + .news-card {
        margin-top: 2em;
        @include media-md {
            margin-top: 0;
            margin-left: 2em;
        }
    }
}
</style>
