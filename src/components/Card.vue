<template lang="">
    <div class="card">
        <div class="img"></div>
        <h3 class="title">Используйте промокод</h3>
        <p class="adress">Ярославль, ул. Пушкина, 15 (543 км)</p>
    </div>
</template>
<script>

export default {
    
}
</script>
<style scoped>
.card {
    width: 309px;
    height: 309px;
    background-color: white;
    background: #FFFFFF;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  cursor: pointer;
    border-radius: 36px;
}

.img {
    width: 309px;
    height: 181px;
    background: #DF6464;
    border-radius: 36px 36px 25px 25px;
}

.title {
    font-size: 16px;
    margin-left: 13px;
    margin-bottom: 40px;

}
.adress {
    margin-left: 13px;
    font-size: 14px;
    max-width: 175px;
}
</style>