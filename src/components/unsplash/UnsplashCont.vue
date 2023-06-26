<template>
  <div class="unsplash__cont container">
    <ul>
      <li v-for="(image, index) in images" :key="index">
        <a :href="`https://unsplash.com/photos/${image.id}`">
          <img :src="image.urls.regular" :alt="image.alt_description" />
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    images: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss">
.unsplash__cont {
  ul {
    column-count: 4;

    li {
      margin-bottom: 20px;
    }
  }
}
// unsplash__search
.unsplash__search {
  margin-bottom: 50px;
  text-align: center;
  input {
    border: 1px solid #e8ecf2;
    font-size: 16px;
    padding: 10px 20px;
    @include border(50px);
    min-width: 300px;
    margin-right: 10px;
  }
  button {
    @include button(#56d8c2, #fff);
    @include border(50px);
  }
}
</style>
