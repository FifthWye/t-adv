<template>
  <header>
    <div class="left-side">
      <span class="logo">t-adv</span>
    </div>
    <div class="right-side">
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
    telegramAuth.setAttribute("data-telegram-login", "t_adv_bot");
    telegramAuth.setAttribute("data-size", "large");
    telegramAuth.setAttribute("data-onauth", "onTelegramAuth(user)");
    telegramAuth.setAttribute("data-request-access", "write");
    document.querySelector("#telegramAuth").appendChild(telegramAuth);
  }
};
</script>

<style scoped>
header {
  width: 100%;
  height: 80px;
  background: #3a6d99;
  display: flex;

  align-items: center;
  justify-content: center;
}

header > .left-side {
  height: 100%;
  width: 100%;
  position: relative;
}

header > .right-side {
  height: 100%;
  width: 100%;
  position: relative;
}

header > .left-side > .logo {
  font-family: "Nanum Gothic", sans-serif;
  font-size: 24px;
  color: #fff;
  position: absolute;
  left: 5%;
  top: 50%;
  -ms-transform: translateY(-50%);
  transform: translateY(-50%);
}

header > .right-side > .auth {
  position: absolute;
  top: 55%;
  -ms-transform: translateY(-50%);
  transform: translateY(-50%);
  right: 5%;
}
</style>