<template>
  <div class="sobre-container" id="sobre">
      <div class="sobre-img">
        <img src='@/assets/logo.png' alt=""/>
      </div>
      <div class="sobre-text">
        <h1>Quem somos?</h1>
        <p>
          O FOR.G.E. iniciou, pois, nós alunos do IFSUL câmpus Charqueadas percebemos que
          podemos render muito mais estudando em grupo pois estaremos compartilhando
          conhecimentos e dificuldades, nós também percebemos que um dos grandes problemas
          para não termos tantos grupos de estudos é a comunicação entre os alunos, e isso faz
          com que ocorra poucos grupos de estudos, e também os poucos que ocorrem são de
          pessoas da mesma sala e série, e isso pode ser um problema pois não tem ninguém que
          já tenha passado por isso antes, já que todos estão no mesmo nível.
        </p>
        <br/>
      </div>
    </div>
</template>
<script>

export default {
  components: {
  },

  data () {
    return {
    }
  },
  watch: {
  }
}
</script>
<style scoped>
  .sobre-container{
    display: flex;
    margin-top: 60px;
    margin-bottom: 60px;
  }

  .sobre-img{
    flex: 1;
    display: flex;
  }
  .sobre-img > img {
    max-width: 80%;
    max-height: 80%;
    margin: 0 auto;

  }
  .sobre-text{
    flex: 1;
    font-family: 'Montserrat', sans-serif;
    text-align: left;
    color: black;
  }
  .sobre-text > h1{
    font-size: 36px;
    margin-bottom: 20px;
    margin-left: 20px;

  }
  .sobre-text > p{
    font-size: 14px;
    line-height: 1.5;
    max-width: 80%;
    margin-left: 30px;

  }

  @media(max-width:739px){
    .sobre-container{
      flex-direction: column;
    }
    .sobre-img{
      margin-top: 30px;
      order: 2;
      margin-bottom: 20px;
    }
    .sobre-img > img {
      max-width: 70%;
      max-height: 70%;
    }
    .sobre-text{
      margin-left: 30px;
    }

  }
</style>
