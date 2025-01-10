<template>
    <div id="closer" class="ri-close-line" @click="closeAll"></div>
</template>

<script>
export default {
    methods: {
        closeAll(){
            this.$emit('close-all');
        }
    }
}
</script>

<style scoped>
    @-webkit-keyframes rotate{
    0%{
        -webkit-transform: rotate(360deg);
        transform: rotate(360deg);
        opacity: 0;
    }
}

    @keyframes rotate{
        0%{
            -webkit-transform: rotate(360deg);
            transform: rotate(360deg);
            opacity: 0;
        }
    }

    #closer{
        position: fixed;
        top: 5rem;
        right: 4rem;
        font-size: 5rem;
        cursor: pointer;
        z-index: 10000;
        color: #5e473e;
        -webkit-animation: rotate .4s linear .4s backwards;
        animation: rotate .4s linear .4s backwards;
        display: block;
    }

    #closer:hover{
        color: #9e7464;
    }

    @media(min-width: 1600px){
    #closer{
        top: 7rem;
        right: 6rem;
    }
}
</style>

