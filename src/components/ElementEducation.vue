<template>
  <div class="education">
    <p class="title">Education</p>
    <ElementSchool
    img="https://i.ibb.co/kHcNYMP/bdx.png"
    diploma="Mathematics and Computing Degree"
    date="Sept 2020 - Now"
    location="Bordeaux, France"
    />
    <ElementSchool
    img="https://i.ibb.co/HtTSYxD/vdg.png"
    diploma="Automatism BTEC Higher National Diploma"
    date="Sept 2018 - July 2020"
    location="Marmande, France"
    />
    <ElementSchool
    img="https://i.ibb.co/HtTSYxD/vdg.png"
    diploma="Computer Science BTEC National Diploma"
    date="Sept 2016 - July 2018"
    location="Marmande, France"
    />
  </div>
</template>

<script>
import ElementSchool from "@/components/ElementSchool.vue";
export default {
  components: {
    ElementSchool,
  },
};
</script>

<style scope>
.education{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 2rem;
  color: #7d7d7d;
}
.title {
  font-size: 2rem;
  font-weight: 400;
  text-align: center;
}
</style>