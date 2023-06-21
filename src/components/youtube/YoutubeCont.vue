<template>
  <main id="main" role="main">
    <section id="youtubePage" className="container">
      <div className="youtube__page">
        <div className="youtube__cont">
          <ul>
            <li v-for="(youtube, index) in youtubes" :key="index">
              <img
                :src="youtube.snippet.thumbnails.medium.url"
                :alt="youtube.snippet.thumbnails.medium.url"
              />
              <span>{{ youtube.snippet.title }}</span>
            </li>
          </ul>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  props: {
    youtubes: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss">
.youtube__cont {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-bottom: 100px;

    li {
      width: 31.3333%;
      margin-bottom: 4%;

      span {
        display: block;
        margin: 4px 0;
        overflow: hidden;
        white-space: nowrap;
        text-overflow: ellipsis;
        -webkit-line-clamp: 1; /* 라인수 */
        -webkit-box-orient: vertical;
        word-wrap: break-word;
      }
      img {
        @include border(5px);
        width: 100%;
        max-height: 280px;
      }
    }
  }
}
</style>
