<template>
    <section class="products">
      <h1 class="title">
        <span>наши продукты</span>
        <a href="#">посмотреть все >></a>
      </h1>
      <div class="box-container">
        <div class="box" v-for="(product, index) in products" :key="index">
          <div class="icons">
            <a href="#" class="ri-shopping-cart-line"></a>
            <a href="#" class="ri-heart-line"></a>
            <a href="" class="ri-eye-line"></a>
          </div>
          <div class="image">
            <img :src="product.image" alt="">
          </div>
          <div class="content">
            <div class="price">{{ product.price }}</div>
            <h3>{{ product.name }}</h3>
            <div class="stars">
              <i class="fas fa-star" v-for="n in 5" :key="n"></i>
              <span> ({{ product.reviews }}) </span>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
 export default {
    data() {
      return {
        products: [
          {
            image: '@/assets/product-1.png',
            price: '₽14000.00',
            name: 'современная мебель',
            reviews: 50
          },
          {
            image: '@/assets/product-2.png',
            price: '₽14000.00',
            name: 'современная мебель',
            reviews: 50
          },
          {
            image: '@/assets/product-3.png',
            price: '₽14000.00',
            name: 'современная мебель',
            reviews: 50
          },
          {
            image: '@/assets/product-4.png',
            price: '₽14000.00',
            name: 'современная мебель',
            reviews: 50
          },
          {
            image: '@/assets/product-5.png',
            price: '₽14000.00',
            name: 'современная мебель',
            reviews: 50
          },
          {
            image: '@/assets/product-6.png',
            price: '₽14000.00',
            name: 'современная мебель',
            reviews: 50
          },
          {
            image: '@/assets/product-7.png',
            price: '₽14000.00',
            name: 'современная мебель',
            reviews: 50
          },
          {
            image: '@/assets/product-8.png',
            price: '₽14000.00',
            name: 'современная мебель',
            reviews: 50
          }
        ]
      };
    }
  };
  </script>


<style scoped>
    .products .box-container{
        display: -ms-grid;
        display: grid;
        -ms-grid-columns: (minmax(26rem, 1fr))[auto-fit];
        grid-template-columns: repeat(auto-fit, minmax(26rem, 1fr));
        gap: 1.5rem;
        padding: 1.5rem;
        border-radius: 3rem;
        background-color: #f0e8e4;
    }

    .products .box-container .box{
        position: relative;
        background: #f5eeeb;
        overflow: hidden;
        border-radius: 2rem;
        border: 0.1rem solid #caab9f;
    }

    .products .box-container .box:hover .image img{
        -webkit-transform: scale(1.2);
        transform: scale(1.2);
    }

    .products .box-container .box:hover .icons{
        top: 0;
    }

    .products .box-container .box .icons{
        position: absolute;
        top: -100%;
        left: 0;
        height: 30rem;
        width: 100%;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        -webkit-box-pack: center;
        -ms-flex-pack: center;
        justify-content: center;
        gap: .5rem;
        background: rgba(242, 242, 242, 0.7);
        z-index: 10;

    }

    .products .box-container .box .icons a{
        text-align: center;
        height: 5rem;
        line-height: 5rem;
        width: 5rem;
        background: #e1cec7;
        color: #5e473e;
        border-radius: 50%;
        font-size: 2rem;
        -webkit-box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.1);
        box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.1);
    }

    .products .box-container .box .icons a:hover{
        background: #5e473e;
        color: #e1cec7;
    }

    .products .box-container .box .image{
        height: 30rem;
        width: 100%;
        overflow: hidden;
    }

    .products .box-container .box .image img{
        height: 30rem;
        width: 100%;
        -o-object-fit: cover;
        object-fit: cover; 
    }

    .products .box-container .box .content{
        padding: 1.5rem 2rem;
    }

    .products .box-container .box .content .price{
        font-size: 1.7rem;
        color: #b58d7e;
    }

    .products .box-container .box .content h3{
        font-size: 2rem;
        color: #5e473e;
        padding: .5rem 0;
    }

    .products .box-container .box .content .stars{
        font-size: 1.7rem;
    }

    .products .box-container .box .content .stars i{
        color: gold;
    }

    .products .box-container .box .content .stars span{
        color: #b58d7e;
    }
</style>