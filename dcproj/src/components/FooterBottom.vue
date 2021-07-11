<template>
  <div>
     <div class="container">
       <div class="button"><a href="#">sign-up now!</a></div>
       <div class="socials">
         <span>follow us</span>
         <a v-for="(e, i) in socialPins" :key="i" :href="e.url">
           <img :src="e.src" :alt="e.alt">
         </a>
       </div>
     </div>
  </div>
</template>

<script>

export default {
  name: 'FooterBottom',
  data() {
    return {
      socialPins: [
        {
          url:"#",
          src:require("./../assets/img/footer-facebook.png"),
          alt:"facebook"
        },
        {
          url:"#",
          src:require("./../assets/img/footer-periscope.png"),
          alt:"periscope"
        },
        {
          url:"#",
          src:require("./../assets/img/footer-pinterest.png"),
          alt:""
        },
        {
          url:"#",
          src:require("./../assets/img/footer-twitter.png"),
          alt:"twitter"
        },
        {
          url:"#",
          src:require("./../assets/img/footer-youtube.png"),
          alt:"youtube"
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>

@import "../style/vars.scss";

.container {
  height: 80px;
  width: 100%;
  background-color: $notgray;
  display: flex;
  justify-content: space-around;

}

.button,
.socials {
  max-height: 50px;
  min-width: 50px;
  transform: translateY(58%);
}

.button {
  a {
    text-transform: uppercase;
    text-decoration: none;
    color: #fff;
    padding: 10px;
    border: 2px solid $dcblue;

    &:hover {
      background-color: $dcblue;
    }
  }
}

.socials {
  span {
    text-transform: uppercase;
    font-weight: 700;
    color: $dcblue;
    padding: 20px;
    position: relative;
    bottom: 20px;
  }
  a {
    position: relative;
    bottom: 10px;

    &:hover img {
      filter: brightness(2);
    }

    &:not(:last-child) {
      margin-right: 10px;
    }
  }
}

</style>