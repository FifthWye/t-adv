<template>
  <header>
    <div class="left-side">
      <router-link to="/">
        <span class="logo">T-ADV</span>
      </router-link>
    </div>
    <div class="right-side">
      <div id="nav">
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
        <router-link to="/catalog">Catalog</router-link>
      </div>
      <div class="auth" id="telegramAuth"></div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data: () => ({}),
  mounted() {
    let telegramAuth = document.createElement("script");
    telegramAuth.setAttribute("async", "");
    telegramAuth.setAttribute(
      "src",
      "https://telegram.org/js/telegram-widget.js?7"
    );

    telegramAuth.setAttribute("data-userpic", "false");
    telegramAuth.setAttribute("data-telegram-login", "t_adv_bot");
    telegramAuth.setAttribute("data-size", "large");
    telegramAuth.setAttribute("data-onauth", "onTelegramAuth(user)");
    telegramAuth.setAttribute("data-request-access", "write");
    document.querySelector("#telegramAuth").appendChild(telegramAuth);
  }
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css?family=Hind&display=swap");

header {
  width: 100%;
  background: #3a6d99;
  display: inline-flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
}

header > .left-side {
  height: 80px;
  width: 45%;
  position: relative;
}

header > .right-side {
  height: 80px;
  width: 55%;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  float: right;
}

header > .left-side > a > .logo {
  font-family: "Hind", sans-serif;
  font-size: 28px;
  color: #fff;
  position: absolute;
  left: 5%;
  top: 50%;
  -ms-transform: translateY(-50%);
  transform: translateY(-50%);
}

header > .right-side > .auth {
  margin-top: 5px;
  margin-right: 5%;
}

header > .right-side > #nav {
  height: 100%;
  line-height: 80px;
  display: flex;
}

header > .right-side > #nav > a {
  height: 100%;
  vertical-align: middle;
  text-decoration: none;
  color: white;
  padding: 0 25px;
}

header > .right-side > #nav > a:hover {
  background-color: rgb(0, 0, 0, 0.1);
}
</style>