<template>
  <div id="MyFirstSlideshow">
    <div class="eg-slideshow">
      <slide>
        <h2>Vue.js Grundkurs</h2>
      </slide>
      <slide :steps="5" enter="bounceInRight" leave="bounceOutDown">
        <h3>
          Was ist
          <div class="inline animated infinite pulse heart"></div>Vue.js?
        </h3>
        <div class="center">
          <eg-transition enter="bounceInLeft" leave="bounceOutLeft">
            <p v-if="step &gt;= 2">
              <b>Vue.js</b> ist ein clientseitiges JavaScript-Webframework.
            </p>
          </eg-transition>
          <eg-transition enter="bounceInRight" leave="bounceOutRight">
            <p v-if="step &gt;= 3">
              <b>Vue.js</b> fokussiert sich auf das View Layer (MVVM).
            </p>
          </eg-transition>
          <eg-transition enter="bounceInLeft" leave="bounceOutLeft">
            <p v-if="step &gt;= 4">
              <b>Vue.js</b> kann mit anderen Libraries kombiniert werden.
            </p>
          </eg-transition>
          <eg-transition enter="bounceInLeft" leave="bounceOutLeft">
            <p v-if="step &gt;= 5">
              <b>Vue.js</b> ist sehr kompakt. (min Variante: ~20 Kilobyte)
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
            <h3>Vue.js Founder:</h3>
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
              <li >
                Arbeitet seit 2016
                <strong>Vollzeit</strong> an Vue.js
              </li>
              </ul>
            </div>
          </eg-modal>
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
