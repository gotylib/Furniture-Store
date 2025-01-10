<script setup>
    import Header from './Header.vue';
    import Footer from './Footer.vue';
    import Heading from './Heading.vue';
    import Category from './Category.vue';
    import Products from './Products.vue';
</script>

<template>
    <main>
        <Header />
        <Heading message="магазин"/>
        <Category />
        <Products />
        <Footer />
    </main>
</template>