<template>
<div>
  <Navbar />
  <Intro />
  <About />
  <Footer />

</div>
</template>
<script>

import Navbar from '../components/navbar.vue'
import Footer from '../components/footer.vue'
import Intro from './home/intro.vue'
import About from './home/about.vue'

export default {
  components: {

    Intro,
    Navbar,
    About,
    Footer
  },

  data () {
    return {
      content: '<h1>Some initial content</h1>',
      image: ''
    }
  },
  watch: {
    content (newValue) {
      console.log('content', this.content)
    }
  }
}
</script>
