<template>
  <form @submit.prevent="" class="search-box">
    <input
      type="search"
      name="search"
      placeholder="What are you looking for?"
    />
    <input type="submit" value="Search" />
  </form>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({});
</script>

<style lang="scss">
@import "./../styles/_variables.scss";

.search-box {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 1rem;
  input {
    display: block;
    appearance: none;
    border: none;
    outline: none;
    background: none;
    &[type="search"] {
      width: 100%;
      color: $brokenWhite;
      background-color: $turquoise;
      font-size: 1.25rem;
      padding: 0.625rem 1rem;
      border-radius: 0.5rem;
      margin-bottom: 0.9375rem;
      transition: 0.4s;
      &::placeholder {
        color: rgba($color: $brokenWhite, $alpha: 0.4);
        font-style: italic;
      }
      &:focus {
        box-shadow: 0rem 0.1875rem 0.375rem rgba(0, 0, 0, 0.2);
      }
      &::-webkit-search-cancel-button {
        &:hover {
          cursor: pointer;
        }
      }
    }

    &[type="submit"] {
      width: 100%;
      max-width: 18.75rem;
      background-color: $h1Green;
      padding: 1rem;
      border-radius: 0.5rem;
      color: $textColorWhite;
      font-size: 1.25rem;
      text-transform: uppercase;
      transition: 0.4s;
      &:active {
        background-color: $lightgreen;
      }
    }
  }
}
</style>
