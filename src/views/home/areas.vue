<template>
      <div  class="Items">
      <h1 class="areas-title">Areas</h1>

      <div class="Item-container">
        <div class="Item">
        <div class="icon">
          <img src='@/assets/elepreto.png' alt=""/>
        </div>
          <h2>Eletrônica</h2>
          <p>
            - Projeto e fabricação de circuitos eletrônicos;<br/>
            - Programação de microcontroladores;<br/>
            - Integração de sistemas.<br/>
          </p>
        </div>
        <div class="Item">
          <div class="icon">
            <img src='@/assets/mecpreto.png' alt=""/>
          </div>
          <h2>Mecânica</h2>
          <p>
            - Projeto mecânico em software CAD;<br/>
            - Usinagem e fabricação mecânica;<br/>
            - Projeto e montagem de mecanismos.<br/>
          </p>
        </div>
        <div class="Item">
          <div class="icon">
            <img src='@/assets/mktpreto.png' alt=""/>
          </div>
          <h2>Marketing</h2>
          <p>
            - Prospecção de patrocínios;<br/>
            - Organização de promoções e eventos;<br/>
            - Criação de conteúdo para redes sociais;<br/>
            - Organização financeira da equipe.<br/>
          </p>
        </div>
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
  * {
    color: black;
  }
  .Item-container{
    display: flex;
    justify-content: center;
    max-width: 960px;
    margin: 30px auto;

  }
  .Item{
    flex: 1;
    flex-direction: column;
    text-align: center;
  }
  .Item > h2{
    font-family: 'Montserrat', sans-serif;
    margin-bottom:20px;
  }
  .Item > p{
    font-family: 'Montserrat', sans-serif;
    padding:0px 15px 15px 15px;
    line-height: 1.25rem;
  }
  .icon{
    flex: 1;
    margin: 0 auto;

  }
  .icon > img{
    max-width: 40%;
    max-height: 40%;
  }
  .areas-title{
    font-family: 'Montserrat', sans-serif;
    text-align: center;
    font-size: 48px;
  }
  @media(max-width:739px){
    .Item-container{
      max-width: 300px;
      flex-direction: column;
    }
    .areas-title{
      font-family: 'Montserrat', sans-serif;
      text-align: center;
      font-size: 36px;

    }

  }
</style>
