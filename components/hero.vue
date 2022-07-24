<template>
 <section class="background_hero hero_image">
        <h2 class="hero__text">AGENCIA KAMISATO </h2>
        <a class="smooth" href="#inicio"><img class="arrow ligth " src="~/assets/arrow.png" alt=""></a>
</section>
</template>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@500&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Abel&family=Lobster&display=swap');
.background_hero{
    width: 100%;
    height: 100vh;
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
}
 .hero_image{
    height: 100vh;
    background-image:linear-gradient(90deg, rgba(115, 160, 228, 0.459) 0%, rgba(78, 113, 255, 0.534) 70%), url("~/assets/hero.jpg");}
.hero__text{
color: #fff;
    text-align: center;
    line-height: 100vh;
    font-family: 'Quicksand', sans-serif;
    font-size: 2rem;
    font-weight: 800;
}
.arrow{
    display: block;
    margin: -100px auto;
    width: 50px;
    height: 50px;
}
.ligth{
    filter: invert();
}
</style>
