<template>
  <div  class="footer">
    <div class="footer-container">
      <div class="footer-info">
        <div class="footer-infos">
        <map-pin-icon size="1.5x" ></map-pin-icon> <p>R. Gen. Balbão, 81 - Centro,<br class="footer-br"> Charqueadas - RS, 96745-000</p>
        </div>
        <div class="footer-infos">
          <mail-icon size="1.5x" ></mail-icon><p> eifchar@acad.charqueadas.ifsul.edu.br</p>
        </div>
        <div class="footer-infos">
          <phone-icon size="1.5x" ></phone-icon><p> +55 (51) 99715-8077</p>
        </div>
      </div>
      <div class="footer-social">
        <p>Redes Sociais</p>
        <div class="footer-icons">
            <a href="https://www.instagram.com/eifchar/"><instagram-icon size="1.5x" class="footer-icon"></instagram-icon></a>
            <a href="https://github.com/EIFCHAR"><github-icon size="1.5x" class="footer-icon"></github-icon></a>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { GithubIcon, InstagramIcon, MapPinIcon, MailIcon, PhoneIcon } from 'vue-feather-icons'

export default {
  components: {
    GithubIcon,
    InstagramIcon,
    MapPinIcon,
    MailIcon,
    PhoneIcon
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
  .footer{
    background-color: #000;
    padding: 30px;
  }
  .footer-container{
    max-width: 960px;
    display: flex;
    margin: 0 auto;
  }
  .footer-info{
    width: 50%;
    color: #fff !important;
  }

  .footer-infos{
    flex: 1;
    display: flex;
    padding: 5px;
    align-items: center;
    font-family: 'Montserrat', sans-serif;
    font-size: 14px;
    width: 100%;
  }
  .footer-infos > p{
    margin-left: 10px;
  }

  .footer-social{
    color: #fff !important;
    display: flex;
    flex-direction: column;
    margin-left: 60px;
    width: 50%;
    align-items: flex-start;

  }
  .footer-social > p{
    margin-bottom:10px;
    font-size: 18px;
    font-weight: bold;
    font-family: 'Montserrat', sans-serif;
  }
  .footer-icon {
    margin-right: 10px;
    color: #fff !important;
  }
  .footer-br{
    display: none;
  }
  @media(max-width:739px){
    .footer-info{
      width: 100%;
    }
    .footer-infos{
      font-size: 12px;
      word-break: break-word;
    }
    .footer-container{
      max-width: 400px;
      flex-direction: column;
    }
    .footer-social{
      margin-top: 30px;
      margin-left: 5px;
    }
    .footer-br{
      display: block;
    }
  }
</style>
