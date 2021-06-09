<template lang="pug">
  section.hero.is-success
    .hero-head
      header.navbar
        .container
          .nav-start
            .nav-item
              strong Platzi Music
          .nav-end.navbar-menu
            router-link.nav-item(:to="{ name: 'search' }") Buscar
            router-link.nav-item(to="/about") Nosotros
        
      .hero-body
        .container.has-text-centered
          h1.title 📻 Platzi Music
          h2.subtitle Canciones que estan en Vue
          pm-player
  
</template>
<script>
import PmPlayer from '@/components/Player.vue'

export default {
  components: { PmPlayer }
}

</script>