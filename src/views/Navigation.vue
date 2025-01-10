<template>
    <!-- navbar start  -->
    <nav ref="navigate" class="navbar" v-bind:class="{ active: isActive }"> 
        <a href="/">главная</a> 
        <a href="/shop">магазин</a> 
        <a href="/about">о нас</a> 
    </nav>
    
    <!-- navbar end  -->

</template>

<script>
export default {
    props: {
        isActive: Boolean
    }
    
}
</script>

<style scoped>
    /* navbar stars */

    .navbar{
        position: fixed;
        top: 1.5%;
        bottom: 1.5%;
        right: -101%;
        z-index: 1000;
        width: 35rem;
        /* height: 100vh; */
        background: #f0e8e4;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        margin: 2%;
        border-radius: 3rem;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        -webkit-box-pack: center;
        -ms-flex-pack: center;
        justify-content: center;
        -webkit-box-orient: vertical;
        -webkit-box-direction: normal;
        -ms-flex-flow: column;
        flex-flow: column;
    }

    .navbar.active{
        right: 0;
        -webkit-box-shadow: 0 0 0 100vw rgba(0, 0, 0, 0.5);
        box-shadow: 0 0 0 100vw rgba(0, 0, 0, 0.5);
        -webkit-transition: .4s linear;
        transition: .4s linear;
    }

    .navbar a{
        margin: 1rem 0;
        font-size: 2.5rem;
        color: #5e473e;
    }

    .navbar a:hover{
        color: #9e7464;
    }

    /* navbar end */
</style>

