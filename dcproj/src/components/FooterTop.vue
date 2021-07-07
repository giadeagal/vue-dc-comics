<template>
  <div>
      <div class="container">
          <div class="flexer">
              <div class="icon" v-for="(e, i) in icons" :key="i">
                  <img :src="e.src" :alt="e.text">
                  <span>{{e.text}}</span>
              </div>
          </div>
      </div>
  </div>
</template>

<script>

export default {
  name: 'FooterTop',
  data() {
      return {
          icons: [
              {
                  src: require("./../assets/img/buy-comics-digital-comics.png"),
                  text:"digital comics"
              },
              {
                  src: require("./../assets/img/buy-comics-merchandise.png"),
                  text:"dc merchandise"
              },
              {
                  src: require("./../assets/img/buy-comics-subscriptions.png"),
                  text:"subscription"
              },
              {
                  src: require("./../assets/img/buy-comics-shop-locator.png"),
                  text:"comic shop locator"
              },
              {
                  src: require("./../assets/img/buy-comics-subscriptions.png"),
                  text:"dc power visa"
              }
          ]
      }
  }
}
</script>

<style lang="scss" scoped>
@import "../style/vars.scss";
.container {
    width: 100%;
    height: 120px;
    background-color: $dcblue;

    .flexer {
        width:70%;
        height: 100%;
        margin:auto;
        display: flex;
        justify-content:space-between;
    }
}

.icon { 
    min-height:70%;
    position:relative;

    &:hover {
        cursor:pointer;
        transform: scale(1.2);
        transition: 200ms;
    }

    span {
        color:white;
        position: relative;
        left: 60px;
        top: 40px
    }

    img {
        max-width: 50px;
        max-height: 50px;
        position:absolute;
        top:25%;
        left:0;
    }
}
</style>