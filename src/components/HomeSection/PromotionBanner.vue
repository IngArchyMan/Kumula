<template>
    <div class="promotion-banner" :class="{ 'hide-banner' : !isVisible }">
        <div class="text-content">
            <p class="banner-text">{{bannerText}}</p>
        </div>
        <span class="icon-action" @click="changeVisibility">
            <i class="fas fa-window-close"></i>
        </span>        
    </div>
</template>

<script>
export default {
    name: 'Promotions',
    data(){
        return{
            isVisible: true,
            bannerText: 'Obtén un 10% de descuento en tu primera compra con el código *Its My first Time*'
        }
    },
    methods:{

        changeVisibility(){
            this.isVisible = !this.isVisible;
        }

    }

}
</script>

<style>
@keyframes move {
  to { transform: translateX(-100%); }
}
.promotion-banner{
    display: flex;
    justify-content: center;
    align-items: center;
}
.promotion-banner.hide-banner{
    display: none;
    visibility: hidden;
}
.text-content{
    width: 90%;
    overflow: hidden;
}
.text-content .banner-text{
    display: block; 
    width: 100%;
    transform: translateX(100%);
  animation: move 20s linear infinite;
}
.icon-action{
    cursor: pointer;
    width: 10%;
}
</style>