<template>
  <div class="school">
    <img :src="this.img" alt="schoolImg" />
    <div class="school-infos">
      <p class="school-infos-diploma">{{this.diploma}}</p>
      <p class="school-infos-date">{{this.date}}</p>
      <P class="school-infos-location">{{this.location}}</P>
    </div>
  </div>
</template>

<script>
export default {  
  props:{
    img:{
      type: String,
      required: true
    },
    diploma:{
      type: String,
      required: true
    },
    date:{
      type: String,
      required: true
    },
    location:{
      type: String,
      required: true
    }
  }
};
</script>

<style scoped>
.school {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  box-shadow: 3px 3px 7px rgba(0, 0, 0, 0.249);
  border-radius: 1rem;
  width: 500px;
  overflow: hidden;
}
.school > img {
  z-index: -1;
  width: 150px;
  aspect-ratio: 2/1;
  border-radius: 1rem;
}
.school-infos{
  width: 100%;
  padding: 5px 6px;
  color: #7d7d7d;
}
.school-infos-diploma{
  font-weight: 700;
  
}
.school-infos-date{
  font-style: italic;
  font-size: 0.8rem;
}
.school-infos-location{
  text-align: end;
  font-size: 0.7rem;
  font-style: italic;
}
@media (max-width: 1000px) {
  .school {
    width: 500px;
    overflow: hidden;
  }
  .school > img {
    z-index: -1;
    width: 150px;
    aspect-ratio: 2/1;
  }
}
</style>