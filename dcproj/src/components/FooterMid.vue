<template>
  <div>
      <div class="container">
        <div class="left">
          <div class="left-one">
            <ul>
            <li>
              <h3>{{list1.title}}</h3>
            </li>
            <li v-for="(e, i) in list1.bullets" :key="i">
              <a :href="list1.url">{{e}}</a>
            </li>
          </ul>
          <ul>
            <li>
              <h3>{{list2.title}}</h3>
            </li>
            <li v-for="(e, i) in list2.bullets" :key="i">
              <a :href="list2.url">{{e}}</a>
            </li>
          </ul>
          </div>
          <div class="left-two">
            <ul>
            <li>
              <h3>{{list3.title}}</h3>
            </li>
            <li v-for="(e, i) in list3.bullets" :key="i">
              <a :href="list3.url">{{e}}</a>
            </li>
          </ul>
          </div>
          <div class="left-three">
            <ul>
            <li>
              <h3>{{list4.title}}</h3>
            </li>
            <li v-for="(e, i) in list4.bullets" :key="i">
              <a :href="list4.url">{{e}}</a>
            </li>
          </ul>
          </div>
        </div>
        <div class="right">
          <img src="./../assets/img/dc-logo-bg.png" alt="">
        </div>
      </div>
  </div>
</template>

<script>

export default {
  name: 'FooterMid',
  data() {
    return {
      list1: {
        title:"dc comics",
        bullets: ["characters", "comics", "movies", "TV", "games", "videos", "news"],
        url: "#"
      },
      list2: {
        title:"shop",
        bullets: ["shop DC", "shop DC collectibles"],
        url: "#"
      },
      list3: {
        title:"dc",
        bullets: ["terms of use", "privacy policy (new)", "ad choices", "advertising", "jobs", "subscriptions", "talent workshops", "CPSC certificates", "ratings", "shop help", "contact us"],
        url: "#"
      },
      list4: {
        title:"sites",
        bullets: ["DC", "MAD magazine", "DC kids", "DC universe", "DC power visa"],
        url: "#"
      }
    }
  }
}
</script>

<style lang="scss" scoped>

.container {
  width: 100%;
  min-height: 300px;
  background-image: url("./../assets/img/footer-bg.jpg");
  display: flex;
  justify-content: center;
}

.right,
.left {
  float:left;
  width: 40%;
  min-height: 100%;
}

.left {
  position: relative;
  font-size: .8rem;

  [class^="left-"] {
    width: calc(100% / 4);
    float: left;

    ul {
      list-style: none;
      float: left;
      padding-right: 50px;

      li {
        margin: 2px 0;

        a {
          color: grey;
          text-decoration: none;
          text-transform: capitalize;

          &:hover {
            color: #fff;
          }
        }
      }
    }
  h3 {
    color: white;
    padding: 10px 0;
    text-transform: uppercase;
  }
  }



}

.right {
  max-height: 300px;
  overflow: hidden;
  
    img{
      width: 80%;
      position: relative;
      bottom: 100px;
      left: 50px;
    }
}

</style>