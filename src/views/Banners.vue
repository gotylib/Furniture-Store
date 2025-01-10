<template>
    <section class="banner-container"> 
        <div class="banner"> 
            <img src="/src/assets/banner-1.jpg" alt=""> 
            <div class="content"> 
                <span>ограниченное предложение</span> 
                <h3>скидка до 50%</h3> 
                <a href="#" class="btn">купить сейчас</a> 
            </div> 
        </div> 
        <div class="banner"> 
            <img src="/src/assets/banner-2.jpg" alt=""> 
            <div class="content"> 
                <span>ограниченное предложение</span> 
                <h3>скидка до 50%</h3> 
                <a href="#" class="btn">купить сейчас</a> 
            </div> 
        </div> 
        <div class="banner"> 
            <img src="/src/assets/banner-3.jpg" alt=""> 
            <div class="content"> 
                <span>ограниченное предложение</span> 
                <h3>скидка до 50%</h3> 
                <a href="#" class="btn">купить сейчас</a> 
            </div> 
        </div> 
         
    </section>   
</template>

<style scoped>
    .banner-container{
    display: -ms-grid;
    display: grid;
    -ms-grid-columns: (minmax(30rem, 1fr))[auto-fit];
    grid-template-columns: repeat(auto-fit, minmax(30rem, 1fr));
    gap: 1.5rem;
}

.banner-container .banner{
    height: 25rem;
    overflow: hidden;
    position: relative;
    border-radius: 3rem;
}

.banner-container .banner img{
    height:  100%;
    width: 100%;
    -o-object-fit: cover;
    object-fit: cover;
}

.banner-container .banner:hover img{
    -webkit-transform: scale(1.2);
    transform: scale(1.2);
}

.banner-container .banner .content{
    position: absolute;
    top: 50%;
    left: 2rem;
    -webkit-transform: translateY(-50%);
    transform: translateY(-50%);
}

.banner-container .banner .content span{
    font-size: 1.7rem;
    color: #b58d7e;
}

.banner-container .banner .content h3{
    padding-top: .5rem;
    font-size: 2.2rem;
    color: #5e473e;
}

.banner-container .banner .content .btn{
    padding: .7rem 2.5rem;
}
</style>

