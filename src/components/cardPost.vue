<template>
  <div>

    <el-card :body-style="{ padding: '0px' }" class="post-card">
      <img :src="post.fields[1].src" class="image-card">
      <div style="padding: 14px;">
        <h2 class="card-title">{{post.fields[0].data}}</h2>
        <div class="bottom clearfix">
          <p class="card-p">
            {{post.fields[2].data}}
          </p>
          <div class="ler-mais-card">
            <a class="ler-mais-card-a" @click="test(post.uuid)">> Ler mais</a>
          </div>
        </div>
      </div>
    </el-card>

  </div>

</template>
<script>

export default {
  components: {
  },
  props: {
    post: {}
  },
  methods: {
    test (uuid) {
      return this.$router.push({ name: 'Post', params: { id: uuid } })
    }
  },
  watch: {
  }
}
</script>

<style scoped>

  .card-title{
    font-family: 'Montserrat', sans-serif;
    color: #000000;
  }
  .card-p{
    font-family: 'Montserrat', sans-serif;
    margin-top: 10px;
    font-size: 12;
    text-align: left;
    line-height: 1.5;
    padding: 5px;
    color: #475669;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 5;
    -webkit-box-orient: vertical;
  }
  .image-card{
    width: 300px;
    height: 200px;
  }
  .post-card{
    width: 300px;
    flex: 1;
    margin-top: 30px;
    margin-left: 10px;
  }
  .ler-mais-card{
    display: inline-block;
    width: 100%;
    text-align: left;
    margin-left: 0;
    margin-right: auto;
  }
  .ler-mais-card-a{
    font-family: 'Montserrat', sans-serif;
    font-size: 14px;
    cursor: pointer;
    text-decoration: none;
    font-weight: bold;
    text-transform: uppercase;
    color:#000000;
  }

</style>
