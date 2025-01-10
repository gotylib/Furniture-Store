<template>
        <section class="services"> 
        <h1 class="title"> <span>Наши услуги</span> <a href="#">Посмотреть все >></a></h1> 
        <div class="box-container"> 
            <div class="box"> 
                <img src="/assets/serv-1.png" alt="Продажа товаров"> 
                <h3>Продажа товаров</h3> 
                <p>Мы предлагаем широкий ассортимент товаров, который удовлетворит любые ваши потребности. Наша команда всегда готова помочь вам с выбором и консультацией.</p> 
                <a href="#" class="btn">Узнать больше</a> 
            </div> 
            <div class="box"> 
                <img src="/assets/serv-2.png" alt="Дизайн продукции"> 
                <h3>Дизайн продукции</h3> 
                <p>Наши дизайнеры создают оригинальные и функциональные решения, которые помогут выделить ваш продукт на рынке. Мы индивидуально подходим к каждому проекту.</p> 
                <a href="#" class="btn">Узнать больше</a> 
            </div> 
            <div class="box"> 
                <img src="/assets/serv-3.png" alt="Круглосуточная поддержка"> 
                <h3>Круглосуточная поддержка</h3> 
                <p>Наша команда поддержки доступна 24/7, чтобы ответить на все ваши вопросы и предоставить необходимую помощь в любое время. Мы всегда рядом!</p> 
                <a href="#" class="btn">Узнать больше</a> 
            </div> 
        </div> 
    </section>
</template>

<style scoped>
    .services .box-container{
    display: -ms-grid;
    display: grid;
    -ms-grid-columns: (minmax(30rem, 1fr))[auto-fit];
    grid-template-columns: repeat(auto-fit, minmax(30rem, 1fr));
    gap: 1.5rem;
    }

    .services .box-container .box{
        padding: 2rem;
        text-align: center;
        background-color: #f0e8e4;
        border-radius: 2rem;
    }

    .services .box-container .box:hover{
        box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
    }

    .services .box-container .box:hover img{
        transform: translateY(-3px);
    }

    .services .box-container .box img{
        font-size: 8rem;
        margin-bottom: 1rem;
    }

    .services .box-container .box h3{
        font-size: 2.2rem;
        color: #5e473e;
    }

    .services .box-container .box p{
        font-size: 1.4rem;
        color: #b58d7e;
        line-height: 2;
        padding: 1rem 0;
    }
</style>