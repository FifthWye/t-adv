<template>
  <div>
    <!-- <img src="../assets/404.png" /> -->
    <div class="err-msg">
      <span>404 - Page not found</span>
      <router-link to="/">Go to home page</router-link>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.err-msg {
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  position: absolute;
  text-align: center;
  align-content: center;
  display: flex;
  flex-wrap: wrap;
}

.err-msg > span {
  width: 100%;
  font-size: 42px;
}
.err-msg > a {
  margin-top: 10px;
  width: 100%;
  color: #3a6d99;
  text-decoration: none;
}
img {
  position: absolute;
  top: 30%;
  left: 20%;
  height: 492px;
  width: 400px;
  opacity: 0.6;
  filter: brightness(50%);
}
</style>