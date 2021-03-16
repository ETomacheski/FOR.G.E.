<template>
  <div id="navbarId">
    <Slide>
      <a href="/">
        <span>Link 1</span>
      </a>
      <a href="/">
        <span>Link 2</span>
      </a>
      <a href="/">
        <span>Link 3</span>
      </a>
    </Slide>
    <img src="@/assets/logo.png" alt="logo" class="logo">
    <div class="navbar">
      <ul class="list">
        <li>
          <a href="/">
            Link 1
          </a>
        </li>
        <li>
          <a href="/">
            Link 2
          </a>
        </li>
        <li>
          <a href="/">
            Link 3
          </a>
        </li>

      </ul>
    </div>
  </div>
</template>
<script>
import { Slide } from 'vue-burger-menu' // import the CSS transitions you wish to use, in this case we are using `Slide`

export default {
  components: {
    Slide // Register your component
  },
  watch: {

  }
}
</script>
<style scoped>
  #navbarId{
    background-color: black;
    display: flex;
    width: 100%;
    height: 55px;
  }
  ::v-deep .bm-burger-button{
    display: none;
  }
  ::v-deep .bm-burger-bars {
      background-color: white;
  }

  .logo{
    width: 250px;
    height: 60px;
    margin-left: 30px;
  }
  .navbar{
    display: flex;
    margin-right: 30px;
    margin-left: auto;
    text-decoration: none;
  }
  li, ul{
    list-style: none;

  }
  .list {
    list-style: none;
    display: flex;
    margin-top: 10px;
  }
  .list > li {
    text-decoration: none;
  }
  .list > li > a{
    text-transform: uppercase;
    padding: 10px;
    display: block;
    text-decoration: none;
    color: #00FA9A;
    font-size: 16px;
    font-family: 'Montserrat', sans-serif;
    margin-right: 10px;
    align-self: right;
    font-weight: 600;
    letter-spacing: 1.5px;
  }
  @media (max-width:739px){
  .logo{
    margin-left: 55px;
  }
  .navbar {
    display: none;
  }
  ::v-deep .bm-burger-button{
    top: 15px !important;
    left: 20px;
    height: 20px;
    width: 30px;
    position: absolute;
    display: block;
  }
}
</style>
