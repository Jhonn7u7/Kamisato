<template>
 <div>
     <nav class="nav" id="inicio">
        <a href="/" class="enlaces">Inicio</a>
        <a href="ganyu" class="enlaces">Noticias</a>
        <a href="#builds" class="enlaces">Builds</a>
    </nav>
 </div>
</template>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@500&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Abel&family=Lobster&display=swap');
.nav{
    background: rgb(0, 0, 0);
    height: 70px;
    padding: 0 50px;
    text-align: right;
    position: sticky;
    top: 0;
    width: 100%;
}

.enlaces{
    color: #fff;
    text-decoration: none;
    line-height: 70px;
    padding: 0 20px;
    display: inline-block;
    font-family: 'Quicksand', sans-serif;
}

.enlaces:hover{
    background: #fff;
    color: rgb(73, 73, 252);
}
</style>
