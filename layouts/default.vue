<template>
    <div id="app" class="d-flex flex-column min-vh-100 bg-light">
      <Header />
      <slot />
      <Footer />
    </div>
</template>
  
  
<script>
    import Header from './header.vue'
    import Footer from './footer.vue'
    export default {
        components: {Header,Footer}
    }
</script>