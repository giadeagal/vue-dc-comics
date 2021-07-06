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


<style scoped>
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
}

li {
  display: inline-block;
  margin: 0 20px;
  padding: 20px 0;
}

a {
  text-decoration: none;
  color: black;
}

/* da mettere in sass */
li:hover {
  border-bottom: 2px solid blue;
}

/* da mettere in sass */
li:hover a {
 color: blue;
}
</style>