<template lang="pug">
  section.hero.is-success
    .hero-head
      header.navbar
        .container
          .navbar-start
            .navbar-item
              strong Platzi Music
          .navbar-end.navbar-menu
            a.navbar-item(@click="selectLang('en')") 🏴󠁧󠁢󠁥󠁮󠁧󠁿  
            a.navbar-item(@click="selectLang('es')") 🇪🇸 
            router-link.navbar-item(to="search") {{ $t('search')}}
            router-link.navbar-item(to="about") {{ $t('about') }}
        
      .hero-body
        .container.has-text-centered
          h1.title 📻 Platzi Music
          h2.subtitle Canciones que estan en Vue
          pm-player
  
</template>
<script>
import PmPlayer from '@/components/Player.vue'

export default {
  components: { PmPlayer },

  methods: {
    selectLang (lang) {
      this.$i18n.locale = lang
    }
  }
}

</script>