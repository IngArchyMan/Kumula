<template>
    <div class="promotion-banner" :class="{ 'hide-banner' : !isVisible }">
        <div class="text-content">
            <p class="banner-text">{{bannerText}}</p>
        </div>
        <span class="icon-action" @click="changeVisibility">
            <i class="fas fa-times"></i>
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
    padding: 0 1rem;
    z-index: 100;
}
.promotion-banner.hide-banner{
    display: none;
    visibility: hidden;
}
.text-content{
    width: calc(100% - 32px);
    overflow: hidden;
}
.text-content .banner-text{
    display: block; 
    width: 1200px;
    transform: translateX(100%);
    animation: move 20s linear infinite;
    margin: 0;
}
.icon-action{
    cursor: pointer;
    width: 32px;
    height: 32px;
    display: flex;
}
.icon-action i{
    font-size: 18px;    
    display: block;
    margin: auto;
}
</style>