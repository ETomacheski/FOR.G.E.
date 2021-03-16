<template>
  <div>
    <h1 class="post-titleCriator">Criar Post</h1>
    <div class="post-selectFild">
      <el-select v-model="selectCurrentOption" placeholder="Select">
        <el-option
          v-for="item in optionsSelectType"
          :key="item"
          :label="item"
          :value="item"
        >
        </el-option>
      </el-select>
      <el-button @click="test" style="margin-left: 10px;"> Adicionar Campo </el-button>
    </div>
    <div v-for="(item, index) in bodyBlog" :key="index" class="post-divConstructor">
      <br>
      <el-input v-if="item.type === 'titulo'" placeholder="Digite o titulo" v-model="bodyBlog[index].data"></el-input>
      <el-input v-if="item.type === 'capa'" placeholder="Digite o link do drive da capa" @change="getSrcDrive(index)" v-model="bodyBlog[index].data"></el-input>
      <el-input v-if="item.type === 'paragrafo'" type="textarea" :rows="2" placeholder="Digite o paragrafo" v-model="bodyBlog[index].data"></el-input>
      <el-input v-if="item.type === 'imagem'" @change="getSrcDrive(index)" placeholder="Digite o link do drive" v-model="bodyBlog[index].data"></el-input>
      <el-input v-if="item.type === 'video'" placeholder="Digite o link do youTube" v-model="bodyBlog[index].data"></el-input>
    </div>

    <br>
    <el-button type="primary" @click="createPost()">Criar Post</el-button>

    <Post :post='bodyBlog' />
  </div>
</template>

<script>
import { mapState } from 'vuex'
import Post from './post/infoPost.vue'
import axios from 'axios'

export default {
  components: {
    Post
  },

  data () {
    return {
      optionsSelectType: [
        'paragrafo',
        'imagem',
        'video'
      ],
      selectCurrentOption: '',
      bodyBlog: [
        {
          type: 'titulo',
          data: '',
          src: ''
        },
        {
          type: 'capa',
          data: '',
          src: ''
        },
        {
          type: 'paragrafo',
          data: '',
          src: ''
        }
      ]
    }
  },
  computed: {
    ...mapState(['token'])
  },
  created () {
    if (this.token === '') return this.$router.push({ name: 'LoginAdmin' })
  },
  methods: {
    getSrcDrive (index) {
      const test = this.bodyBlog[index].data.split('/')
      this.bodyBlog[index].src = `https://docs.google.com/uc?id=${test[5]}`
    },
    test () {
      if (this.selectCurrentOption === '') return

      this.bodyBlog.push({
        type: this.selectCurrentOption,
        data: '',
        src: ''
      })
      this.selectCurrentOption = ''
    },
    async createPost () {
      const params = {
        fields: this.bodyBlog
      }

      await axios({
        method: 'post',
        url: 'https://eifchar-api.herokuapp.com/createPost',
        data: params,
        headers: {
          token: this.token
        },
        withCredentials: true
      })
      return this.$router.push({ name: 'adminHome' })
    }
  },

  watch: {
    bodyBlog: function () {

    }
  }
}
</script>

<style scoped>
.post-divConstructor{
  width: 960px;
  margin: 10px auto;
}
.post-selectFild {
  padding: 10px;
}
.post-titleCriator {
  color: black;
  font-family: 'Montserrat', sans-serif;

}
</style>
