<template>
  <div>
    <div class="container">

      <a href="#"><img src="@/assets/img/dc-logo.png" alt="logo DC"></a>

      <nav>
        <ul>
          <li v-for="(item, i) in navItems " :key="i"><a :href="item.url">{{item.text}}</a></li>
        </ul>
      </nav>

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
          url:"#"
        },
        {
          text:"comics",
          url:"#"
        },
        {
          text:"movies",
          url:"#"
        },
        {
          text:"tv",
          url:"#"
        },
        {
          text:"games",
          url:"#"
        },
        {
          text:"collectibles",
          url:"#"
        },
        {
          text:"videos",
          url:"#"
        },
        {
          text:"fans",
          url:"#"
        },
        {
          text:"news",
          url:"#"
        },
        {
          text:"shop",
          url:"#"
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
}

img {
  max-height: 100%;
}

ul {
  list-style: none;
  font-weight: 700;
  text-transform: uppercase;

  li {
  display: inline-block;
  margin: 0 20px;
  padding: 20px 0;

    &:hover {
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

</style>