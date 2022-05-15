<template>
<div class="container">
    <!-- <div class="selector">
        <p class="selector-text" :class="{'active': !this.selector}" >Projects</p>
        <SelectorBtn @toggle="toggle" />
        <p class="selector-text" :class="{'active': this.selector}" >About</p>
    </div> -->
    <p>My projects</p>
    <DisplayProjects class="element" :class="{'show': !this.selector}"/>
    <!-- <DisplayAbout  class="element" :class="{'show': this.selector}"/> -->
</div>

</template>

<script>
// import SelectorBtn from "@/components/SelectorBtn.vue"
import DisplayProjects from "./DisplayProjects.vue"
// import DisplayAbout from "./DisplayAbout.vue"
export default {
    components:{
        // SelectorBtn,
        DisplayProjects,
        // DisplayAbout
    },
    data() {
        return {
            selector: false
        }
    },
    methods:{
        toggle(){
            this.selector = !this.selector
        }
    }

}
</script>

<style scoped>
p{
    text-align: center;
}
.container{
    margin-bottom: 3rem;
}
.active{
    color: black !important;
    transition-duration: 1.5s;
}
.selector-text{
    transform: translateY(-2px);
    color: #c9c9c9;
    transition-duration: 1s;
}
.selector{
    display: none;
    flex-direction: row;
    justify-content: center;
    align-content: center;
    gap: 1rem;

    margin-top: 1.5rem;
}
.element{
    position: absolute;
    visibility: hidden;
    opacity: 0;

}
.show{
    position: static;
    visibility: visible;
    opacity: 1;
    transition-duration: 1s;
}

@media (max-width: 1000px) {
  .selector{

    margin-top: 0.5rem;
    }
  }
</style>