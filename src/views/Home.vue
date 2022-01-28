<template>
  <main class="home">
    <article class="feature__card">
      <router-link to="/movie/movieIdIsWhat!!!"
        ><img
          src="http://placekitten.com/200/300"
          alt="Image Description"
          class="feature__card__img"
        />
        <aside class="feature__card__details">
          <h3>Title</h3>
          <p>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nesciunt,
            praesentium voluptatum. Blanditiis, sequi optio. Ex explicabo soluta
            labore sit porro voluptatum obcaecati, earum hic doloribus, officia
            dignissimos quisquam eaque cumque.
          </p>
        </aside>
      </router-link>
    </article>
    <search-box />
    <movies-list />
  </main>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import SearchBox from "./../components/SearchBox.vue";
import MoviesList from "./../components/MoviesList.vue";

export default defineComponent({
  components: {
    SearchBox,
    MoviesList,
  },
});
</script>

<style lang="scss">
@import "./../styles/_variables.scss";

.home {
  .feature__card {
    position: relative;
    &__img {
      display: block;
      width: 100%;
      height: 18.75rem;
      object-fit: cover;
      position: relative;
      z-index: 0;
    }

    &__details {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      background-color: rgba($color: #000000, $alpha: 0.6);
      padding: 1rem;
      z-index: 1;

      h3 {
        color: $textColorWhite;
        margin-bottom: 1rem;
      }

      p {
        color: $textColorWhite;
      }
    }
  }
}
</style>
