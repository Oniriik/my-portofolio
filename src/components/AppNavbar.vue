<template>
    <nav class="container">
        <p>Timothé Lim</p>
        <div class="link" @click.prevent="scrolldown">
            <p>Contact</p>
            <img src="@/assets/img/arrow.png" alt="arrow">
        </div>
       
    </nav>
</template>

<script>
export default {
    methods: {
        scrolldown(){
            const page = document.getElementsByClassName("page-wrapper")[0]
            console.log(page.scrollHeight)
            window.scrollTo(0,page.scrollHeight);
        }
    },
}
</script>

<style scoped>

nav{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    height: 3rem;


}
.link{
    font-size: 1rem;
    font-weight: 400;
}
</style>