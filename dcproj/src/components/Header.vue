<template>
  <div>
    <div class="container">

      <a href="#"><img src="@/assets/img/dc-logo.png" alt="logo DC"></a>

      <nav>
        <ul>
          <li v-for="(item, i) in navItems " :key="i" :class="{active : item.active}"><a :href="item.url">{{item.text}}</a></li>
        </ul>
      </nav>

    </div>

    <div class="jumbo">
        <img src="@/assets/img/jumbotron.jpg" alt="">
    </div>

    
  </div>
</template>

<script>

export default {
  name: 'Header',
  data() {
    return {
      navItems: [
        {
          text:"characters",
          url:"#",
          active: false
        },
        {
          text:"comics",
          url:"#",
          active: true
        },
        {
          text:"movies",
          url:"#",
          active: false
        },
        {
          text:"tv",
          url:"#",
          active: false
        },
        {
          text:"games",
          url:"#",
          active: false
        },
        {
          text:"collectibles",
          url:"#",
          active: false
        },
        {
          text:"videos",
          url:"#",
          active: false
        },
        {
          text:"fans",
          url:"#",
          active: false
        },
        {
          text:"news",
          url:"#",
          active: false
        },
        {
          text:"shop",
          url:"#",
          active: false
        }
      ]
    }
  }
}
</script>


<style lang="scss" scoped>
@import "../style/vars.scss";
.container {
  display: flex;
  justify-content: space-around;
  height: 80px;
  position:relative;
}

a {
  img {
  max-height: 100%;
  }
}

ul {
  list-style: none;
  font-weight: 700;
  text-transform: uppercase;

  li {
  display: inline-block;
  margin: 0 20px;
  padding: 20px 0;

    &:hover,
    &.active {
    border-bottom: 2px solid $dcblue;

      & a {
      color: $dcblue;
      }
    }
  }

  a {
  text-decoration: none;
  color: black;
  }
}

.jumbo{
  width: 100%;
  max-height: 350px;
  overflow: hidden;

  img {
    max-width: 100%;
  }
}

.current {
  display: inline-block;
  background-color: $dcblue;
  padding:10px;
  color:#fff;
  text-transform: uppercase;
  border-radius: 4px;
  position:absolute;
  top: 50%;
  left: 5rem;
}

</style>