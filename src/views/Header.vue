<template>
    <header class="header"> 
    <a href="home.html" class="logo"><i class="ri-store-2-line"> Риан </i></a> 
    <form action="#" class="search-form"> 
        <input type="search" placeholder="поиск здесь..." id="search-box"> 
        <label for="search-box" class="ri-search-line"></label> 
    </form> 

    <div class="icons"> 
        <div id="menu-btn" class="ri-menu-line" @click="toggleActive('menu')"></div> 
        <div id="search-btn" class="ri-search-line"></div> 
        <div id="cart-btn" class="ri-shopping-cart-line" @click="toggleActive('cart')"></div> 
        <div id="login-btn" class="ri-user-line" @click="toggleActive('login')"></div> 
    </div> 
    </header>
    <Navigation :isActive="isActiveMenu" />
    <ShoppingCard :isActive="isActiveCart"/>
    <LoginForm :isActive="isActiveLoginForm"/>
    <CloseButton v-show="showCloseButton" @close-all="CloseAllActive"/>
</template>

<script>
    import Navigation from './Navigation.vue';
    import LoginForm from './LoginForm.vue';
    import ShoppingCard from './ShoppingCard.vue';
    import CloseButton from './CloseButton.vue';
    export default {
    components: {
        Navigation,
        LoginForm,
        ShoppingCard,
        CloseButton
    },
    data() {
        return {
        isActiveMenu: false,
        isActiveCart: false,
        isActiveLoginForm: false

        }
    },
    computed: {
        showCloseButton(){
            console.log(this.isActiveMenu || this.isActiveCart || this.isActiveLoginForm)
            return this.isActiveMenu || this.isActiveCart || this.isActiveLoginForm; // Показываем кнопку, если хотя бы один компонент активен 
        }
    },
    methods: {
        toggleActive(component) {
            if (component === 'menu') { 
                this.isActiveMenu = !this.isActiveMenu; 
            } else if (component === 'cart') { 
                this.isActiveCart = !this.isActiveCart; 
            } else if (component === 'login') { 
                this.isActiveLoginForm = !this.isActiveLoginForm; 
            } 
        },
        CloseAllActive() {
            console.log('close')
            this.isActiveMenu = false;
            this.isActiveCart = false;  
            this.isActiveLoginForm = false;
        }
        

    }
    }
</script>


<style scoped>
    .header{
    padding: 2rem 9%;
    position: -webkit-sticky;
    position: sticky;
    top: 0;
    left: 0;
    right: 0;
    z-index: 100;
    background: #f0e8e4;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    -webkit-box-pack: justify;
    -ms-flex-pack: justify;
    justify-content: space-between;
    border-radius: 0 0 2rem 2rem;
    }
    .header .logo{
        font-size: 2.5rem;
        color: #5e473e;
        font-weight: 500;
    }

    .header .logo i{
        padding-right: .3rem;
    }

    .header .search-form{
        height: 5rem;
        width: 50rem;
        border-radius: .75rem;
        background-color: transparent;
        overflow: hidden;
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        background: #f0e8e4;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
        border: 0.1rem solid #caab9f;
    }

    .header .search-form input{
        height: 100%;
        width: 100%;
        padding: 0 1.2rem;
        font-size: 1.6rem;
        color: #5e473e;
        text-transform: none;
        background: transparent;
    }

    .header .search-form input::placeholder{
        color: #5e473e;
    }

    .header .search-form label{
        font-size: 2.2rem;
        padding-right: 1.7rem;
        cursor: pointer;
        color: #5e473e;
    }

    .header .search-form label:hover{
        color: #9e7464;
    }

    .header .icons{
        display: flex;
        align-items: center;
    }

    .header .icons div{
        margin-left: 2rem;
        font-size: 2.5rem;
        cursor: pointer;
        color: #5e473e;
    }

    .header .icons div:hover{
        color: #9e7464;
    }
    
    #search-btn {
        display: none;
    }
</style>