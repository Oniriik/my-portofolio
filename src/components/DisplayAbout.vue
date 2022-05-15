<template>
<div class="about">
    <ElementEducation/>
    <p>Skills</p>
</div>
</template>

<script>
import ElementEducation from '@/components/ElementEducation.vue'
export default {
    components:{
        ElementEducation
    }
}
</script>

<style scoped>
.about{
    margin-top: 2rem;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    gap: 2rem;
}




@media (max-width: 1000px) {
  .about{
    margin-top: 1rem;
    flex-direction: column;
}
  }
</style>