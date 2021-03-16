<template>
  <div class="campus-container">
      <div class="campus-img">
        <img src='@/assets/if.jpg' alt=""/>
      </div>
      <div class="campus-text">
        <h1>IFSUL Charqueadas</h1>
        <p>
          A EIFCHAR é uma equipe de eficiência energética criada no final de
          2018 por alunos do Instituto Federal Sul-rio-grandense Campus
          Charqueadas, composta em sua maioria por alunos do Ensino Médio Técnico.
        </p>
        <br/>
        <p >
        É no Instituto Federal Sul-rio-grandense Campus Charqueadas que
        desenvolvemos todos os dias nosso projeto. O Campus oferece
         desde 2006 diversos cursos gratuitos como técnico integrado
          Mecatrônica, técnico integrado em Informática, técnico integrado
          em Fabricação Mecânica (PROEJA). E também os cursos superiores de
          Tecnólogo em Sistemas para Internet (TSI), Engenharia de Controle
          e Automação,  pós-graduação em Educação e Contemporaneidade
          (especialização) e o Mestrado Profissional em Educação Profissional
          e Tecnológica em Rede.
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
  .campus-container{
    display: flex;
    margin-top: 60px;
  }

  .campus-img{
    flex: 1;
    display: flex;
  }
  .campus-img > img {
    max-width: 85%;
    max-height: 85%;
    margin: 0 auto;
    margin-bottom: 30px;
    border:solid 1px;
    /* box-shadow: 20px 20px white, 23px 23px #FBB900; */

  }
  .campus-text{
    flex: 1;
    font-family: 'Montserrat', sans-serif;
    text-align: left;
    color: black;
  }
  .campus-text > h1{
    font-size: 36px;
    margin-bottom: 20px;
    margin-left: 20px;
  }
  .campus-text > p{
    font-size: 14px;
    line-height: 1.5;
    max-width: 80%;
    margin-left: 30px;
  }

  @media(max-width:739px){
    .campus-container{
      flex-direction: column;
    }
    .campus-img{
      margin-top: 30px;
      order: 2;
      margin-bottom: 20px;
    }
    .campus-img > img {
      max-width: 70%;
      max-height: 70%;
    }
    .campus-text{
      margin-left: 30px;
    }

  }
</style>
