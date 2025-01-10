<template> 
    <section class="home">  
        <div class="slides-container">  
            <div 
                class="slide" 
                v-for="(slide, index) in slides" 
                :key="index" 
                :class="{ active: currentSlide === index }"
            >   
                <div class="content">   
                    <span>{{ slide.subtitle }}</span>   
                    <h3>{{ slide.title }}</h3>   
                    <p>{{ slide.description }}</p>   
                    <a href="#" class="btn">купить сейчас</a>   
                </div>   
                <div class="image">   
                    <img :src="slide.image" alt="">   
                </div>   
            </div>  
        </div>  
        <div @click="nextSlide" id="slide-next" class="ri-arrow-right-line"></div>  
        <div @click="prevSlide" id="slide-prev" class="ri-arrow-left-line"></div>  
    </section>  
</template>

<script>
export default {
    data() {
        return {
            currentSlide: 0,
            slides: [
                {
                    subtitle: 'новые поступления',
                    title: 'современное кресло',
                    description: 'Откройте для себя идеальное сочетание стиля и комфорта в нашем современном кресле.',
                    image: '/src/image/home-img-1.png'
                },
                {
                    subtitle: 'новые поступления',
                    title: 'классическое кресло',
                    description: 'Наслаждайтесь комфортом и элегантностью нашего классического кресла.',
                    image: '/src/image/home-img-2.png'
                },
                // Добавьте больше слайдов по мере необходимости
            ]
        };
    },
    methods: {
        nextSlide() {
            this.currentSlide = (this.currentSlide + 1) % this.slides.length; // Переход к следующему слайду
        },
        prevSlide() {
            this.currentSlide = (this.currentSlide - 1 + this.slides.length) % this.slides.length; // Переход к предыдущему слайду
        }
    }
};
</script>

<style scoped>
    @-webkit-keyframes fadeOut{
    0%{
        -webkit-transform: scale(0.5);
        transform: scale(0.5);
        opacity: 0;
        }
    }

    @keyframes fadeOut {
        0%{
            -webkit-transform: scale(0.5);
            transform: scale(0.5);
            opacity: 0;
        }
    }

    @-webkit-keyframes fadeLeft{
        0%{
            -webkit-transform: translateX(-5rem);
            transform: translateX(-5rem);
            opacity: 0;
        }
    }

    @keyframes fadeLeft {
        0%{
            -webkit-transform: translateX(-5rem);
            transform: translateX(-5rem);
            opacity: 0;
        }
    }

    .home{
        position: relative;
        margin: 2%;
        border-radius: 3rem;
        background-color: #f0e8e4;
    }

    .home .slides-container .slide{
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        -ms-flex-align: wrap;
        flex-wrap: wrap;
        gap: 1.5rem;
        display: none;
    }

    .home .slides-container .slide.active{
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
    }

    .home .slides-container .slide .content{
        -webkit-box-flex: 1;
        -ms-flex: 1 1 40rem;
        flex: 1 1 40rem;
        -webkit-animation: fadeLeft .4s linear .4s backwards;
        animation: fadeLeft .4s linear .4s backwards ;
    }

    .home .slides-container .slide .content span{
        font-size: 2.5rem;
        color: #b58d7e;
    }

    .home .slides-container .slide .content h3{
        font-size: 6rem;
        color: #5e473e;
    }

    .home .slides-container .slide .content p{
        font-size: 1.5rem;
        color: #b58d7e;
        padding: .5rem 0;
        text-transform: none;
    }


    .home .slides-container .slide .content .image{
        -webkit-box-flex: 1;
        -ms-flex: 1 1 40rem;
        flex: 1 1 40rem;
        padding: 3rem 0;
    }

    .home .slides-container .slide .content .image .img{
        width: 100%;
        -webkit-animation: fadeOut .4s linear;
        animation: fadeOut .4s linear;
    }

    .home #slide-next,
    .home #slide-prev{
        position: absolute;
        top: 50%;
        -webkit-transform: translateY(-50%);
        transform: translateY(-50%);
        height: 5rem;
        width: 5rem;
        line-height: 5rem;
        font-size: 3rem;
        text-align: center;
        color: #845f51;
        background: #e1cec7;
        cursor: pointer;
        border-radius: 50%;
    }

    .home #slide-next:hover,
    .home #slide-prev:hover{
        background: #845f51;
        color: #e1cec7;
    }

    .home #slide-next{
        right: 2rem;
    }

    .home #slide-prev{
        left: 2rem;
    }
</style>