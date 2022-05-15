<template>
  <div class="link">
      <a :href="this.href" target="blank" :style="{ fontSize: this.size }" >{{text}}</a>
      <img src="@/assets/img/arrow.png" alt="arrow">
  </div>
</template>

<script>
export default {
    props:{
        text:{
            type : String,
            required: true
        },
        href:{
            type : String,
            required: true
        },
        size:{
            type : String,
            required: true
        }
    },
    methods:{
        linkHref(){
            window.location.href = this.href;
        }
    }
}
</script>

<style>
.link{
    display:flex;
    flex-direction: row;
    align-items: center;
    gap: 5px;
    font-family: 'Mulish', sans-serif;
    font-weight: 800;
    font-size: 1.2rem;
    cursor: pointer;
}
.link > img{
    width: 10px;
    height: auto;
    transform: translateY(2px);
}
</style>