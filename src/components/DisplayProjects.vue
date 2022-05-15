<template>
  <div class="projects">
    <ElementProject
      title="Spotify Dump"
      img="https://i.ibb.co/mHVRypS/spotify.png"
      stack="Vuejs v3, Vuex"
      desc="Spotify API based app that allows users to get their top tracks in a picture form to share on socials."
      href="https://spotify-dump.xyz/"
      accentColor="#2FBF57"
      secondColor="#BFADD5"
    />
    <ElementProject
      title="U-Bordeaux Verif"
      img="https://i.ibb.co/HtgSpp2/Group-1.png"
      stack="Js, DiscordJs"
      desc="Discord Bot that verify student emails by sending verification token to the student's email then check it."
      href="https://github.com/Oniriik/U-Bordeaux-Verif"
      accentColor="#3EB6E9"
      secondColor="#cca079"
    />
    <ElementProject
      title="Allo'Cinoche"
      img="https://i.ibb.co/znQrRwH/allocinoche.png"
      stack="ExpressJs, Ejs, Strapi"
      desc="Website that reference movies/series. Users can add items via + button. It use movie-database-alternative to add new content."
      href="https://github.com/Oniriik/U-Bordeaux-Verif"
      accentColor="#8E3248"
      secondColor="#7979cc"
    />
    <ElementProject
      title="My portofolio"
      img="https://i.ibb.co/Vj2khvH/folio.png"
      stack="Vuejs v3"
      desc="My personnal portofolio made from scratch."
      href="#"
      accentColor="#79ccb2"
      secondColor="#F7A59D"
    />
  </div>
</template>

<script>
import ElementProject from "@/components/ElementProject.vue";

export default {
  components: {
    ElementProject,
  },
};
</script>

<style>
.projects{
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 2rem;
    margin-top: 2rem;
}
@media (max-width: 1000px) {
  
    .projects{
      grid-template-columns: 1fr;
      margin-top: 1rem;
    }   
  }
</style>