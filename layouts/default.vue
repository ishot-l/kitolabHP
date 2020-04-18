<template>
  <b-container fluid="md" class="shadow">

    <Header />

    <b-sidebar id="sidebar-1" title="メニュー" right shadow>
      <div class="px-3 py-2">
        <p>
          メニューが入ります
        </p>
        <b-img src="https://picsum.photos/500/500/?image=54" fluid thumbnail></b-img>
      </div>
    </b-sidebar>

    <nuxt />

    <Footer />

  </b-container>
</template>

<script>
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Header,
    Footer
  }
}
</script>

<style scoped>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
}

.bg {
  background-color: gray;
}

.container-md {
  padding-left: 0;
  padding-right: 0;
}
</style>
