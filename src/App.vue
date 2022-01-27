<template>
  <header>
    <router-link to="/">
      <h1><span>Vue</span>Movies</h1>
    </router-link>
  </header>
  <router-view />
</template>

<style lang="scss">
@import "./styles/_variables.scss";

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Fira Sans", sans-serif;

  &::selection {
    background: transparentize($color: $h1Green, $amount: 0.5);
  }

  body {
    background: $bodyBg;
  }

  a {
    text-decoration: none;
  }

  header {
    display: flex;
    align-content: center;
    justify-content: center;
    padding: 0.625rem 1rem;
    background-color: $headerBg;
    box-shadow: 0 0 0.4375rem rgba($color: #000000, $alpha: 0.2);

    h1 {
      color: $textColorWhite;
      font-size: $h1Size;

      span {
        color: $h1Green;
      }
    }
  }
}
</style>
