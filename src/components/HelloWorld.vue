<template lang="pug">
.newsContainer
  .newsFlex
    .newsItem(v-for="item in news")
      .newsImg(:style="{ 'background-image': 'url(' + item.img + ')' }")
      .newsTitle {{ item.title }}
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      news: [
        {
          img:
            " https://ipta.nthu.edu.tw/wp-content/uploads/2020/10/banner-768x292.png ",
          title: "yo!shout out to sam",
        },
        {
          img: "https://ipta.nthu.edu.tw/wp-content/uploads/2020/05/200528.jpg",
          title: "yo!shout out to sam",
        },
        {
          img:
            "https://ipta.nthu.edu.tw/wp-content/uploads/2020/10/banner-768x292.png ",
          title: "yo!shout out to sam",
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass">
.newsFlex
  display: flex
  flex-direction: row
  border: 3px solid #ccc
  width: 1000px
  height: 200px
  margin: auto
  justify-content: space-between
.newsItem
  //border: 1px solid red
  width: 260px
  height: 300px

  flex-direction: column
  justify-content: space-between

.newsImg
  //border: 1px solid blue
  width: 100%
  height: 300px
  backgroud-size: cover
  border-radius: 10px
  margin-bottom: 28px
</style>
