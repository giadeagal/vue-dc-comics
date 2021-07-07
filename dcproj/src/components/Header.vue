<template>
  <div>
    <div class="container">

      <a href="#"><img src="@/assets/img/dc-logo.png" alt="logo DC"></a>

      <nav>
        <ul>
          <li><a href="#">Ciccio</a></li>
          <li><a href="#">Bello</a></li>
          <li><a href="#">Pippo</a></li>
        </ul>
      </nav>

    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
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