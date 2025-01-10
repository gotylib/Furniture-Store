<template>
    <section class="about">  
    <div class="image">  
        <img src="/src/image/about-img.jpg" alt="">  
    </div>  
    <div class="content">  
        <span>добро пожаловать в наш магазин</span>  
        <h3>мы делаем ваш дом более уютным</h3>  
        <p>Наша компания основана с целью создавать уникальные предметы интерьера, которые придают вашему дому особый стиль и уют. Мы стремимся использовать только высококачественные материалы и современные технологии, чтобы каждый продукт отвечал самым высоким стандартам. С 2010 года мы работаем на рынке и зарекомендовали себя как надежный партнер для многих клиентов.</p>
        <p>Мы гордимся тем, что наша команда состоит из талантливых дизайнеров и мастеров, которые стремятся к совершенству в каждом проекте. Наша миссия — сделать ваш дом не только красивым, но и комфортным. Присоединяйтесь к числу наших довольных клиентов и позвольте нам помочь вам создать идеальное пространство для жизни!</p>
        
        <a href="#" class="btn">читать далее</a>  
    </div>  
    </section>
</template>

<style scoped>
    .about{
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
    gap: 2rem;
    margin: 2%;
    border-radius: 3rem;
    background-color: #f0e8e4;
    }

    .about .image{
        -webkit-box-flex: 1;
        -ms-flex: 1 1 40rem;
        flex: 1 1 40rem;
    }

    .about .image img{
        border-radius: 2rem;
        width: 100%;
    }

    .about .content{
        -webkit-box-flex: 1;
        -ms-flex: 1 1 40rem;
        flex: 1 1 40rem;
    }

    .about .content span{
        font-size: 2rem;
        color: #b58d7e;
    }

    .about .content h3{
        font-size: 2.5rem;
        color: #5e473e;
        padding-top: 1rem;
    }

    .about .content p{
        font-size: 1.4rem;
        color: #b58d7e;
        padding: 1rem 0;
        line-height: 2;
        text-transform: none;
    }
</style>