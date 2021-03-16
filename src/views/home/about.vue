<template>
  <div class="sobre-container" id="sobre">
      <div class="sobre-img">
        <img src='@/assets/logo.png' alt=""/>
      </div>
      <div class="sobre-text">
        <h1>Quem somos?</h1>
        <p>
          A EIFCHAR é uma equipe de eficiência energética criada no final de
          2018 por alunos do Instituto Federal Sul-rio-grandense Campus
          Charqueadas, composta em sua maioria por alunos do Ensino Médio Técnico.
        </p>
        <br/>
        <p >
          Participamos pela primeira vez da Shell Eco-marathon em 2019 com o
          protótipo denominado Eletro 3. Buscamos desenvolver tecnologias
          sustentáveis e com alta  eficiência energética na construção
          de veículos super econômicos.
        </p>
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
