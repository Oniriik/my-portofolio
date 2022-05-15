<template>
  <div class="contact container">
    <p class="message">Get in touch with me</p>
    <ElementLink
      size="2rem"
      text="contact@timothelim.me"
      href="mailto: contact@timothelim.me"
    />
    <div class="links">
      <ElementLink
        size="1rem"
        text="Github"
        href="https://github.com/Oniriik"
      />
      <ElementLink
        size="1rem"
        text="Linkedin"
        href="https://linkedin.com/in/timothelim"
      />
    </div>
  </div>
</template>

<script>
import ElementLink from "@/components/ElementLink.vue";
export default {
  components: {
    ElementLink,
  },
};
</script>

<style scoped>
.message {
  color: black;
  font-weight: bold;
}
.links{
    display: flex;
    flex-direction: row;
    gap: 1rem;
    margin-bottom: 2rem;
}
</style>