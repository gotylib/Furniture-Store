<template>
    <div class="shopping-cart" :class="{ active: isActive }"> 
 
    <div class="box"> 
        <i class="ri-close-line close-icon"></i> 
        <img src="/src/assets/cart-img-1.jpg" alt=""> 
        <div class="content"> 
            <h3>современная мебель</h3> 
            <span class="quantity"> 1 </span> 
            <span class="multiply"> x </span> 
            <span class="price"> $140.00 </span> 
        </div> 
    </div> 
    <div class="box"> 
        <i class="ri-close-line close-icon"></i> 
        <img src="/src/assets/cart-img-2.jpg" alt=""> 
        <div class="content"> 
            <h3>современная мебель</h3> 
            <span class="quantity"> 1 </span> 
            <span class="multiply"> x </span> 
            <span class="price"> $140.00 </span> 
        </div> 
    </div> 
    <div class="box"> 
        <i class="ri-close-line close-icon"></i> 
        <img src="/src/assets/cart-img-3.jpg" alt=""> 
        <div class="content"> 
            <h3>современная мебель</h3> 
            <span class="quantity"> 1 </span> 
            <span class="multiply"> x </span> 
            <span class="price"> $140.00 </span> 
        </div> 
    </div> 
    <div class="box"> 
        <i class="ri-close-line close-icon"></i> 
        <img src="/src/assets/cart-img-4.jpg" alt=""> 
        <div class="content"> 
            <h3>современная мебель</h3> 
            <span class="quantity"> 1 </span> 
            <span class="multiply"> x </span> 
            <span class="price"> $140.00 </span> 
        </div> 
    </div> 
    <h3 class="total"> итог: <span>$560.00</span></h3> 
    <a href="#" class="btn">оформить заказ</a> 
    </div> 
</template>


<script>
export default {
    props: {
        isActive: Boolean
    }
}
</script>

<style scoped>
    .shopping-cart{
        position: fixed;
        top: 1.5%;
        bottom: 1.5%;
        right: -101%;
        z-index: 1000;
        width: 35rem;
        /* height: 100vh; */
        background: #f0e8e4;
        padding: 2rem;
        padding-top: 8rem;
        overflow-y: scroll;
        margin: 2%;
        border-radius: 3rem;
    }

    .shopping-cart.active{
        right: 0;
        -webkit-box-shadow: 0 0 0 100vw rgba(0, 0, 0, 0.5);
        box-shadow: 0 0 0 100vw rgba(0, 0, 0, 0.5);
        -webkit-transition: .4s linear;
        transition: .4s linear;
    }

    .shopping-cart::-webkit-scrollbar{
        width: 0;
    }

    .shopping-cart::-webkit-scrollbar-track{
        background: #eae0dc;
    }

    .shopping-cart::-webkit-scrollbar-thumb{
        background: #b58d7e;
    }

    .shopping-cart .box{
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        gap: 1.5rem;
        position: relative;
        margin-bottom: 1rem;
        padding: .75em;
        background-color: #faf7f6;
        border-radius: 1rem;
    }

    .shopping-cart .box .close-icon{
        position: absolute;
        top: 50%;
        right: 1rem;
        -webkit-transform: translateY(-50%);
        transform: translateY(-50%);
        font-size: 2rem;
        color: #5e473e;
        cursor: pointer;
    }

    .shopping-cart .box .close-icon:hover{
        color: #9e7464;
    }

    .shopping-cart .box img{
        border-radius: .65rem;
        height: 8rem;
    }

    .shopping-cart .box .content h3{
        color: #5e473e;
        font-size: 1.8rem;
        padding-bottom: .5rem;
    }

    .shopping-cart .box .content span{
        font-size: 1.5rem;
        color: #b58d7e;
    }

    .shopping-cart .box .content span.multiply{
        margin: 0 1rem;
    }

    .shopping-cart .total{
        text-align: center;
        font-size: 2rem;
        padding: 1rem 0;
        color: #845f51;
    }

    .shopping-cart .total span{
        color: #5e473e;
    }

    .shopping-cart .btn{
        width: 100%;
        text-align: center;
    }
</style>


