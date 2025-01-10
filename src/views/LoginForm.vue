<template>
    <div class="login-form" :class="{ active: isActive }"> 
        <form action="#"> 
            <h3>форма входа</h3> 
            <input type="email" placeholder="введите ваш email" class="box"> 
            <input type="password" placeholder="введите ваш пароль" class="box"> 
            <div class="remember"> 
                <input type="checkbox" class="remember-me"> 
                <label for="remember-me">запомнить меня</label> 
            </div> 
            <input type="submit" value="войти сейчас" class="btn"> 
            <p>забыли пароль? <a href="#">нажмите здесь</a></p> 
            <p>нет аккаунта? <a href="#">создайте сейчас</a></p> 
        </form> 
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
    .login-form{
    position: fixed;
    top: 1.5%;
    bottom: 1.5%;
    right: -101%;
    z-index: 1000;
    width: 35rem;
    /* height: 100vh; */
    background: #f0e8e4;
    padding: 2rem;
    margin: 2%;
    border-radius: 3rem;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    justify-content: center;
}

.login-form.active{
    right: 0;
    -webkit-box-shadow: 0 0 0 100vw rgba(0, 0, 0, 0.5);
    box-shadow: 0 0 0 100vw rgba(0, 0, 0, 0.5);
    -webkit-transition: .4s linear;
    transition: .4s linear;
}

.login-form form{
    padding: 1.7rem;
    border: 0.1rem solid #caab9f;
    border-radius: 2rem;
}

.login-form h3{
    font-size: 2.2rem;
    padding-bottom: 1rem;
    color: #5e473e;
}

.login-form form .box{
    width: 100%;
    text-transform: none;
    font-size: 1.5rem;
    color: #5e473e;
    padding: 1rem 1.2rem;
    border: 0.1rem solid #caab9f;
    margin: .7rem 0;
    border-radius: .75rem;
    background: transparent;
}

.login-form form .box::placeholder{
    color: #845f51;
}

.login-form form .remember{
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    gap: .5rem;
}

.login-form form .remember label{
    padding: 1rem 0;
    cursor: pointer;
    font-size: 1.5rem;
    color: #b58d7e;
}

.login-form form .btn{
    width: 100%;
    margin: 1rem 0;
    text-align: center;
}

.login-form form p{
    padding-top: 1rem;
    font-size: 1.4rem;
    color: #b58d7e;
}

.login-form form p a{
    color: #5e473e;
}

.login-form form p a:hover{
    text-decoration: underline;

}
</style>

