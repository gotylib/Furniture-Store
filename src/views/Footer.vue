<template>
    <section class="footer"> 
        <div class="box-container"> 
            <div class="box"> 
                <h3>Быстрые ссылки</h3> 
                <a href="/"> <i class="ri-arrow-right-line"></i> главная </a> 
                <a href="/shop"> <i class="ri-arrow-right-line"></i> магазин </a> 
                <a href="/about"> <i class="ri-arrow-right-line"></i> о нас </a> 
            </div> 
            <div class="box"> 
                <h3>Дополнительные ссылки</h3> 
                <a href="#"> <i class="ri-arrow-right-line"></i> мой заказ </a> 
                <a href="#"> <i class="ri-arrow-right-line"></i> мой список желаемого </a> 
                <a href="#"> <i class="ri-arrow-right-line"></i> мой аккаунт </a> 
                <a href="#"> <i class="ri-arrow-right-line"></i> мои избранные </a> 
                <a href="#"> <i class="ri-arrow-right-line"></i> команда пользователей </a> 
            </div> 
            <div class="box"> 
                <h3>Социальные сети</h3> 
                <a href="#"> <i class="ri-facebook-fill"></i> facebook </a> 
                <a href="#"> <i class="ri-twitter-fill"></i> twitter </a> 
                <a href="#"> <i class="ri-instagram-fill"></i> instagram </a> 
                <a href="#"> <i class="ri-linkedin-box-fill"></i> linkedin </a> 
                <a href="#"> <i class="ri-pinterest-fill"></i> pinterest </a> 
            </div> 
 
            <div class="box"> 
                <h3>Рассылка</h3> 
                <p>Подпишитесь на последние обновления</p> 
                <form action="#"> 
                    <input type="email" placeholder="введите ваш email" id=""> 
                    <input type="submit" value="подписаться" class="btn"> 
                </form> 
            </div> 
        </div> 
    </section>
</template>

<style scoped>
    .footer{
    margin: 2%;
    border-radius: 3rem;
    background: #f0e8e4;
    }

    .footer .box-container{
        display: -ms-grid;
        display: grid;
        -ms-grid-columns: (minmax(25rem,1fr))[auto-fit];
        grid-template-columns: repeat(auto-fit,minmax(25rem, 1fr));
        gap: 1.5rem;
    }

    .footer .box-container .box .h3{
        font-size: 2.2rem;
        color: #5e473e;
        padding: 1rem 0;
    }

    .footer .box-container .box p{
        font-size: 1.6rem;
        color: #b58d7e;
        padding: 1rem;
    }

    .footer .box-container .box a{
        font-size: 1.4rem;
        color: #5e473e;
        padding: 1rem 0;
        display: block;
        display: flex;
        align-items: center;
    }

    .footer .box-container .box a:hover{
        color: #9e7464;
    }

    .footer .box-container .box a:hover i{
        padding-right: 2rem;
    }

    .footer .box-container .box a i{
        padding-right: .5rem;
        color: #5e473e;
        font-size: 1.7rem;
    }

    .footer .box-container .box form input[type="email"]{
        width: 100%;
        padding: 1rem 1.2rem;
        font-size: 1.6rem;
        color: #5e473e;
        text-transform: none;
        margin: .7rem 0;
        background: transparent;
        border-radius: .75rem;
        border: 0.1rem solid #caab9f;
    }

    .footer .box-container .box form input[type="email"]::placeholder{
        color: #5e473e;
    }
</style>