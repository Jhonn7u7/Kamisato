<template>
 <section class="background_hero hero_image">
        <h2 class="hero__text">Build Ayaka </h2>
</section>
</template>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@500&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Abel&family=Lobster&display=swap');
.background_hero{
    width: 60%;
    height: 100vh;
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
}
 .hero_image{
    height: 90vh;
    background-image:linear-gradient(90deg, rgba(55, 75, 105, 0.459) 0%, rgba(33, 43, 80, 0.534) 70%), url("~/assets/hero-aya.jpg");}
.hero__text{
color: #fff;
    text-align: left;
    line-height: 10vh;
    font-family: 'Quicksand', sans-serif;
    font-size: 2rem;
    font-weight: 800;
}
</style>
