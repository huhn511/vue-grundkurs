<template>
  <div id="MyFirstSlideshow">
    <div class="eg-slideshow">
      <slide :steps="5" enter="bounceInRight" leave="bounceOutDown">
        <h2>Vue.js Grundkurs</h2>
        <eg-transition enter="bounceInRight" leave="bounceOutRight">
          <p v-if="step &gt;= 2">
            <b>Was ist Vue?</b>
          </p>
        </eg-transition>
        <eg-transition enter="bounceInLeft" leave="bounceOutLeft">
          <p v-if="step &gt;= 3">
            <b>Die Geschichte.</b>
          </p>
        </eg-transition>
        <eg-transition enter="bounceInRight" leave="bounceOutRight">
          <p v-if="step &gt;= 4">
            <b>Die Grundlagen.</b>
          </p>
        </eg-transition>
        <eg-transition enter="bounceInLeft" leave="bounceOutLeft">
          <p v-if="step &gt;= 5">
            <b>Live Coding.</b>
          </p>
        </eg-transition>
      </slide>
      <slide :steps="6" enter="bounceInRight" leave="bounceOutDown">
               <h3>
          Was ist
          <div class="inline animated infinite pulse heart"></div>Vue.js?
        </h3>
       <iframe class="center" src="https://vuejs.org/" width="100%" height="800px" frameborder="0"></iframe>
      </slide>
      <slide :steps="6" enter="bounceInRight" leave="bounceOutDown">
        <h3>
          <div class="inline animated infinite pulse heart"></div>Also, Vue.js ...
        </h3>
        <div class="center">
          <eg-transition enter="bounceInLeft" leave="bounceOutLeft">
            <p v-if="step &gt;= 2">
              ... ist ein <b>clientseitiges</b> JavaScript-<b>Webframework</b>.
            </p>
          </eg-transition>
          <eg-transition enter="bounceInRight" leave="bounceOutRight">
            <p v-if="step &gt;= 3">
              ... fokussiert sich auf das <b>View Layer</b> (MVVM).
            </p>
          </eg-transition>
          <eg-transition enter="bounceInLeft" leave="bounceOutLeft">
            <p v-if="step &gt;= 4">
              ... kann mit <b>anderen Libraries</b> sehr gut <b>kombiniert</b> werden.
            </p>
          </eg-transition>
          <eg-transition enter="bounceInRight" leave="bounceOutLeft">
            <p v-if="step &gt;= 5">
              ... ist sehr <b>kompakt</b> (min Variante: <b>~20 Kilobyte</b>).
            </p>
          </eg-transition>
          <eg-transition enter="bounceInLeft" leave="bounceOutLeft">
            <p v-if="step &gt;= 6">
              ... ist sehr <b>Einsteigerfreundlich</b>. :-)
            </p>
          </eg-transition>
        </div>
      </slide>

      <slide :steps="5" enter="bounceInDown">
        <h3>Noch ein Javascript Framework?</h3>
        <eg-transition enter="fadeIn" leave="fadeOut">
          <div class="trio" v-if="step &gt;=2">
            <div class="img_wrapper">
              <img src="@/assets/logos/angular.png">
            </div>
            <h4>Angular</h4>
            <iframe
              class="github-star"
              src="https://ghbtns.com/github-btn.html?user=angular&amp;repo=angular&amp;type=star&amp;count=true&amp;size=large"
              frameborder="0"
              scrolling="0"
              width="160px"
              height="30px"
            ></iframe>
            <p>by Google</p>
            <p>"One framework. Mobile & desktop."</p>
          </div>
        </eg-transition>
        <eg-transition enter="fadeIn" leave="fadeOut">
          <div class="trio" v-if="step &gt;=3">
            <div class="img_wrapper">
              <img src="@/assets/logos/react.png">
            </div>
            <h4>React</h4>
            <iframe
              class="github-star"
              src="https://ghbtns.com/github-btn.html?user=facebook&amp;repo=react&amp;type=star&amp;count=true&amp;size=large"
              frameborder="0"
              scrolling="0"
              width="160px"
              height="30px"
            ></iframe>
            <p>by Facebook</p>
            <p>"A JavaScript library for building user interfaces"</p>
          </div>
        </eg-transition>

        <eg-transition enter="fadeIn" leave="fadeOut">
          <div class="trio" v-if="step &gt;=4">
            <div class="img_wrapper">
              <img src="@/assets/logos/vue.png">
            </div>
            <h4>Vue.js</h4>
            <iframe
              class="github-star"
              src="https://ghbtns.com/github-btn.html?user=vuejs&amp;repo=vue&amp;type=star&amp;count=true&amp;size=large"
              frameborder="0"
              scrolling="0"
              width="160px"
              height="30px"
            ></iframe>
            <p>by Community</p>
            <p>"The Progressive JavaScript Framework"</p>
          </div>
        </eg-transition>
      </slide>
      <slide enter="zoomIn" leave="fadeOut">
        <h3>Was nun?</h3>
        <div class="center">
          <img class="the_hardest_decison" src="https://i.chzbgr.com/full/5410066176/hE4D57265/">
        </div>
      </slide>
      <slide enter="bounceInDown">
        <eg-transition enter="fadeIn" leave="fadeOut">
          <eg-modal>
            <h3>Github stars chart:</h3>
            <div class="center">
              <img src="../../assets/github_stars_chart.png" :style="{width: '100%'}">
            </div>
          </eg-modal>
        </eg-transition>
      </slide>
      <slide enter="bounceInDown">
        <eg-transition enter="fadeIn" leave="fadeOut">
          <eg-modal>
            <h3>Vue.js Creator:</h3>
            <div class="center" :style="{display: 'flex'}">
              <div :style="{width: '50%'}">
                <img src="../../assets/evan_you.jpg" :style="{height: '10em'}">
                <h3>Evan You</h3>
              </div>
              <ul class="list">
                <li>
                  Hat bei Google als
                  <strong>Creative Technologist</strong> gearbeitet.
                </li>
                <li>
                  Core Developer bei
                  <strong>Meteor</strong>
                </li>
                <li>
                  Arbeitet seit 2016
                  <strong>Vollzeit</strong> an Vue.js
                </li>
              </ul>
            </div>
          </eg-modal>
        </eg-transition>
      </slide>
      <slide :steps="6" enter="bounceInRight" leave="bounceOutDown">
        <h2>Vue.js Ecosystem</h2>
        <eg-transition enter="bounceInRight" leave="bounceOutRight">
          <p v-if="step &gt;= 2">
            <a href="https://github.com/vuejs/vue-cli">vue-cli</a>
            - Project scaffolding
          </p>
        </eg-transition>
        <eg-transition enter="bounceInLeft" leave="bounceOutLeft">
          <p v-if="step &gt;= 3">
            <a href="https://github.com/vuejs/vue-router">vue-router</a>
            - Single-page application routing
          </p>
        </eg-transition>
        <eg-transition enter="bounceInRight" leave="bounceOutRight">
          <p v-if="step &gt;= 4">
            <a href="https://github.com/vuejs/vuex">vuex</a>
            - Large-scale state management
          </p>
        </eg-transition>
        <eg-transition enter="bounceInLeft" leave="bounceOutLeft">
          <p v-if="step &gt;= 5">
            <a href="https://github.com/vuejs/vue-devtools">vue-devtools</a>
            - Browser DevTools extension
          </p>
        </eg-transition>
        <eg-transition enter="bounceInLeft" leave="bounceOutLeft">
          <p v-if="step &gt;= 6">
            <a href="https://github.com/vuejs/awesome-vue">Awesome Vue.js</a>
            - Und viel, viel mehr!
          </p>
        </eg-transition>
      </slide>
      <slide :steps="7" enter="bounceInRight" leave="bounceOutDown">
        <h2>Live Coding</h2>
        <eg-transition enter="bounceInRight" leave="bounceOutRight">
          <p v-if="step &gt;= 2">
            Eine App vom Erstellen zum Deploy:
            (<a
              target="_blank"
              href="https://huhn511.github.io/buddybuilder/#/"
            >100in100</a>).
          </p>
        </eg-transition>
        <eg-transition enter="bounceInRight" leave="bounceOutRight">
          <p v-if="step &gt;= 3">Neues Projekt mit vue-cli</p>
        </eg-transition>
        <eg-transition enter="bounceInRight" leave="bounceOutRight">
          <p v-if="step &gt;= 4">Inputs und Data Binding.</p>
        </eg-transition>
        <eg-transition enter="bounceInRight" leave="bounceOutRight">
          <p v-if="step &gt;= 5">Button mit Clickhandler.</p>
        </eg-transition>
        <eg-transition enter="bounceInRight" leave="bounceOutRight">
          <p v-if="step &gt;= 6">Componenten selbst schreiben.</p>
        </eg-transition>
        <eg-transition enter="bounceInRight" leave="bounceOutRight">
          <p v-if="step &gt;= 7">Kurze Einführung in IOTA.</p>
        </eg-transition>
      </slide>
      <slide :steps="4" enter="bounceInRight" leave="bounceOutDown">
        <h2>Coole Projekte</h2>
        <eg-transition enter="bounceInRight" leave="bounceOutRight">
          <p v-if="step &gt;= 2">
            <a target="_blank" href="https://zulko.github.io/eaglejs-demo/">Eagle.js</a> - A slideshow framework for hackers.*
          </p>
        </eg-transition>
        <eg-transition enter="bounceInRight" leave="bounceOutRight">
          <p v-if="step &gt;= 3">
            <a target="_blank" href="https://www.vuestorefront.io/">Vue Storefront</a> - PWA for eCommerce. 100% offline, platform agnostic, headless, Magento 2 supported.
          </p>
        </eg-transition>
        <eg-transition enter="bounceInRight" leave="bounceOutRight">
          <p v-if="step &gt;= 4">
            <a target="_blank" href="https://vuepress.vuejs.org/">VuePress</a> - Minimalistic Vue-powered static site generator.
          </p>
        </eg-transition>
        <eg-transition enter="bounceInRight" leave="bounceOutRight">
          <p v-if="step &gt;= 2" class="bottom">* Diese Seite wure mit Eagle.js erstellt.</p>
        </eg-transition>
      </slide>
    </div>
  </div>
</template>

<script>
import eagle from "eagle.js";
export default {
  mixins: [eagle.slideshow],
  infos: {
    // These infos appear on the home page, below the slideshow's thumbnail
    title: "Vue.js Introduction",
    description: "Ein Vue.js Grundkurs",
    path: "vue-introduction"
  }
};
</script>

<style lang='scss'>
@import url(https://fonts.googleapis.com/css?family=Patrick+Hand+SC);
#MyFirstSlideshow {
  .eg-slideshow {
    font-family: "Patrick Hand SC";
    background-color: #eef;
    .eg-slide {
      .eg-slide-content {
        width: 25em;
        max-width: 80%;
        margin: 0 auto;
      }
    }
  }
  .eg-slide-content {
    width: 25em;
    max-width: 80%;
    margin: 0 auto;
  }

  .trio {
    text-align: center;
    width: 30%;
    float: left;
    justify-content: center;
    margin: 10px;
    .img_wrapper {
      padding: 0 auto;
      height: 100px;
      img {
        margin: 0 auto;
        width: 100px;
        margin: 20px auto;
      }
    }
  }
  .list {
    text-align: left;
    font-size: 1.5em;
  }
}
</style>
