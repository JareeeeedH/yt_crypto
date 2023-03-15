<template>
  <nav>
    <div class="yt-logo">
      <img src="@/assets/yt_logo.jpeg" alt="logo" />
    </div>

    <a>關於我們</a>
    <a style="margin-right: auto">聯絡我們</a>

    <router-link to="/">登入</router-link>
    <router-link to="/about">註冊</router-link>｜ &nbsp;
    <img class="qa-mark" src="@/assets/icon/question.png" />
  </nav>
</template>

<style lang="scss" scoped>
.yt-logo {
  width: 100px;
  margin-right: 20px;
  img {
    width: 100%;
  }
}

.qa-mark {
  width: 30px;
}

nav {
  display: flex;
  padding: 15px;
  // justify-content: left;
  align-items: center;

  a {
    text-decoration: none;
    font-weight: bold;
    padding: 10px;
    color: rgba(0, 0, 0, 0.55);

    cursor: pointer;

    &.router-link-exact-active {
      color: #4e41b5;
    }
  }
}
</style>
