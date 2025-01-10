<template>
    <section class="heading">  
    <h3>наш магазин</h3>  
    <p><a href="/">главная</a>/ <span>{{ message }}</span></p>  
</section>
</template>

<script>
export default {
    props: {
        message: String
    }
}
</script>
