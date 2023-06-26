<template>
  <div>UnsplashSearch</div>
</template>

<style lang="scss">
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
