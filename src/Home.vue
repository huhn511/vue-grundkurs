<template lang='pug'>
.frontpage
  .content
    h1
      span.logo
      span Vue
      span.grey .js
    h2 The Progressive JavaScript Framework

    iframe.github-star(src="https://ghbtns.com/github-btn.html?user=vuejs&repo=vue&type=star&count=true&size=large"
                       frameborder="0" scrolling="0" width="160px" height="30px")
    p.
      Vue.js ist ein <strong>clientseitiges JavaScript-Webframework</strong>
      zum Erstellen von <strong>Single-Page-Webanwendungen</strong> nach dem MVVM-Muster

    p.
      Diese Slides geben dir einen Unberblick und helfen dir Webseiten und Apps mit Vue.js zu erstellen. Viel Spaß!

    .thumbnails
      .box-card(v-for='slideshow in slideshows')
        router-link(:to='slideshow.infos.path' @click.native="click")
          .embedded-slideshow-container
            component(:is="slideshow", :embedded='true',
                      :keyboardNavigation='false',
                      :mouseNavigation='false')
        .caption
          h3 {{slideshow.infos.title}}
          p.thumbnail-description {{slideshow.infos.description}}
</template>

<script>
import slideshows from './slideshows/slideshows.js'

export default {
  data: function () {
    return {
      slideshows: slideshows.list
    }
  },
  mounted: function () {
    document.currentSlide = {}
  },
  methods: {
    click: function (evt) {
      evt.stopPropagation()
    }
  }
}
</script>

<style lang='scss' scoped>
@import url(https://fonts.googleapis.com/css?family=Patrick+Hand+SC);

.frontpage {
  width: 100%;
  height: auto;
  position: absolute;
  background-image: assetUrl("~eagle.js/dist/themes/assets/crossword.png");
  .content{
    width: 600px;
    max-width: 90%;
    margin: 0 auto;
  }
}

h1, h2, h3, h4, p {
  font-weight: normal;
  font-family: 'Patrick Hand SC'
}

h1 {
  font-size: 8em;
  margin-top: 0.5em;
  margin-bottom: 0;
  line-height: 0.8em;
  text-align: center;
}
h2 {
  font-size: 2.2em;
  margin-top: 0.4em;
  margin-bottom: 2em;
  line-height: 0.8em;
  text-align: center;
}

p {
  margin-top: 1.5em;
  font-size: 23px;
}
h3 {
  font-size: 30px;
}

.grey {
  color: #bbb
}

.box-card {
  text-align: center;
  margin-bottom: 50px;
  .embedded-slideshow-container {
    position: relative;
    width: 150px;
    height: 120px;
    margin: 0 auto;
    border: 1px solid grey;
    overflow: hidden;
  }
  h3, p {
    margin-bottom: 0;
    margin-top: 0;
  }
}

a {
  text-decoration: inherit;
  color: inherit;
}

.logo {
  display: inline-block;
  width: 100%;
  height:90px;
  margin-right: 0.1em;
  background-image: url(assets/logos/vue.png);
  background-size: contain;
  background-position: center bottom;
  background-repeat: no-repeat;
}

.github-star {
  display: block;
  margin: 0 auto;
  margin-top: -10px;
}
</style>
