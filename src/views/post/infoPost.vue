<template>
  <div style="margin-bottom: 50px;">
    <div v-for="(item, index) in post" :key="index" class="container-post">
      <h1 v-if="item.type === 'titulo'" class="post-title">{{item.data}}</h1>
      <img v-if="item.type === 'capa' && item.src !== ''" :src="item.src" alt="" class="post-cover">
      <p v-if="item.type === 'paragrafo'" class="post-text">{{item.data}}</p>
      <img v-if="item.type === 'imagem'" :src="item.src" alt="" class="post-cover">
      <iframe v-if="item.type === 'video'" class="post-cover"
        :src="item.data"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      ></iframe>
    </div>

  </div>
</template>

<script>

export default {
  components: {
  },

  props: {
    post: Array
  },
  methods: {

  },
  watch: {

  }
}
</script>

<style scoped>

  .post-title{
    color: black;
    font-family: 'Montserrat', sans-serif;
    text-align: center;
    font-size: 48px;
    margin-top: 20px;
    margin-bottom: 20px;
  }
  .post-cover{
    width: 960px;
    height: 600px;
  }
  .post-text{
    color: black;
    font-family: 'Montserrat', sans-serif;
    width: 960px;
    margin: 20px auto;
    text-align: left;
    line-height: 1.5;
  }
  @media(max-width:739px){

    .container-post{
      max-width: 300px;
      margin-right:auto ;
      margin-left:auto;
    }
    .post-cover{
      width: 300px;
      height: 200px;
    }
    .post-text{

      width: 300px;
    }
  }

</style>
