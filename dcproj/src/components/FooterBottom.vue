<template>
  <div>
     <div class="container">
       <div class="button"></div>
       <div class="socials"></div>
     </div>
  </div>
</template>

<script>

export default {
  name: 'FooterBottom'
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
  background-color: teal;
  transform: translateY(25%);
}

</style>