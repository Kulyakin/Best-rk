<template>
    <div class="main">
        <Carousel/>
        <Carousel/>
        <Carousel/>
    </div>
</template>
<script>
import Carousel from './Carousel.vue';
import Card from './Card.vue';

export default {
    components: { Carousel, Card }
}
</script>
<style scoped>
    .main {
        width: 414px;
        background-color: #D9D9D9;
    }
</style>