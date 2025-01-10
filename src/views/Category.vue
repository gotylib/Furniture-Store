<template>
        <section class="category">  
        <h1 class="title"> <span>наши категории</span> <a href="#">посмотреть все >></a> </h1>  
        <div class="box-container">  
            <a href="#" class="box">  
                <img src="/src/image/icon-1.png" alt="">  
                <h3>диван для дома</h3>  
            </a>  
            <a href="#" class="box">  
                <img src="/src/image/icon-2.png" alt="">  
                <h3>рабочий стол</h3>  
            </a>  
            <a href="#" class="box">  
                <img src="/src/image/icon-3.png" alt="">  
                <h3>угловой стол</h3>  
            </a>  
            <a href="#" class="box">  
                <img src="/src/image/icon-4.png" alt="">  
                <h3>офисный стул</h3>  
            </a>  
            <a href="#" class="box">  
                <img src="/src/image/icon-5.png" alt="">  
                <h3>новый шкаф</h3>  
            </a>  
        </div>  
    </section>
</template>

<style scoped>
    .category .box-container{
    display: -ms-grid;
    display: grid;
    -ms-grid-columns: (minmax(16rem, 1fr))[auto-fit];
    grid-template-columns: repeat(auto-fit, minmax(16rem, 1fr));
    gap: 1.5rem;
    }

    .category .box-container .box{
        padding: 2rem;
        text-align: center;
        border-radius: 2rem;
        color: #f0e8e4;
    }

    .category .box-container .box:hover{
        box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
    }

    .category .box-container .box:hover img{
        transform: translateY(-3px);
    }

    .category .box-container .box img{
        height:  6rem;
        margin-bottom: 1rem;
    }

    .category .box-container .box h3{
        font-size: 1.7rem;
        color: #5e473e;
    }
</style>
