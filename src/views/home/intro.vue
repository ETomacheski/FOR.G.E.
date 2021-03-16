<template>
  <div class="backgroundColor">
    <main class="intro">
      <img :src="homeImgSrc" class="img" alt="">
      <h1 class="teste">FORGE  <br/>  FORmando Grupo de Estudos</h1>
    </main>
  </div>
</template>
<script>
import homeImg from '@/assets/imghome.png'

export default {
  components: {
  },

  data () {
    return {
      homeImgSrc: homeImg
    }
  },
  watch: {
  }
}
</script>
<style scoped>

  body, h1, h2, h3, p, ul {
    padding: 0px;
    margin: 0px;
    -ms-overflow-style: -ms-autohiding-scrollbar;

  }
  a{
    text-decoration: none;
    color: white;
  }
  * {
    box-sizing: border-box;
  }
  .img{
    max-width: 50%;
  }
  .listDiv{
    align-self: flex-end;
    flex: 1;
    float: right;
    list-style: none;
    align-self: center;
    align-items: flex-end;
    text-align: right;
  }
  .list{
    list-style: none;
    display: flex;
    justify-content: flex-end;
  }

  .intro {
    background-size: cover;
    width: 100%;
    height: 90vh;
    text-align: center;
    display: flex;
    opacity: 0.9;
  }
  .intro > * {
    opacity: 1 !important;
  }
  .teste {
    font-size: 48px;
    margin: auto auto;
    font-family: 'Montserrat', sans-serif;
    color: #00FA9A;
    font-weight: bold;
  }

  @media(max-width:739px){
    .intro{
      padding: 100px 0;
      display: flex;
      align-items: center;
      flex-direction: column;
      height: 40vh;

    }
    .intro h1 {
      font-size: 1.5em;
      max-width: 350px;
      align-items: center;
    }

  }

  .backgroundColorDrawer{
    background-color: #252525;
    height: 100%;
  }

  .ListDrawer{
    padding: 10px;
    display: block;
    color: #FBB900;
    font-size: 1.225em;
    font-family: 'Montserrat', sans-serif;
    margin-right: 0px;
    align-self: right;

  }
  .CloseDrawer{
    color: #fff;
    margin-right: 'auto';
    margin-left: 0;
  }
</style>
