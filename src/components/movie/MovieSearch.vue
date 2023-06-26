<template>
  <div class="movie__search container">
    <h2 class="blind">검색하기</h2>
    <input
      ref="inputRef"
      @keypress="onKeyPress"
      type="search"
      placeholder="영화를 검색해보세요!"
    />
    <button type="submit" @click="onClick">검색하기</button>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup(props) {
    const inputRef = ref(null);

    const handleSearch = () => {
      const value = inputRef.value;
      props.onSearch(value);
    };

    const onKeyPress = (event) => {
      if (event.key === "Enter") {
        handleSearch();
      }
    };

    const onClick = () => {
      handleSearch();
    };

    return {
      inputRef,
      onKeyPress,
      onClick,
    };
  },
};
</script>

<style lang="scss">
// movie__search
.movie__search {
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
