<template>
    <div class="sevices-section">
        <div class="content-section">
            <div class="up">
                <h1 class="title-section">Title Services</h1>
                <p class="subtitle-section">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Tempora, fuga accusantium, quia minus autem vero magni repudiandae et, reiciendis debitis numquam natus illo delectus? Veritatis nam magnam explicabo porro soluta!</p>
            </div>
            <div class="middle">
                <div class="wrapper_middle">
                    <div class="on-section first-section">
                        <div class="bg-overlay">
                            <figure>
                                <img src="@/assets/img/services-sect-one.png" alt="Servicio de construcción">
                            </figure>                            
                        </div>
                        <p class="tile-on-section">Construcción</p>
                        <p class="subtile-on-section">Subtitle-section</p>
                        
                        <div class="on-section-actions">
                            <p class="describe-section">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Veritatis, excepturi autem debitis adipisci ipsam eos. Eaque similique aspernatur minus aliquid, illo vero, eum optio nemo temporibus explicabo consequatur quod distinctio?</p>
                            <div class="buttons-action-section">
                                <button class="btn prp-btn showme-more">Ver Proyectos</button>
                                <button class="btn snd-btn contact-me">Contactar a ventas</button>
                            </div>
                            
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'Services',
}
</script>
<style>
.sevices-section{
    width: 100%;
    height: fit-content;
}
.sevices-section .content-section{
    position: relative;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    flex-wrap: wrap;
    height: 100%;
    padding: 4rem 10px;
}
.up{
    text-align: center;
}
.sevices-section .content-section .up .title-section{
    font-size: 130px;
    text-transform: uppercase;
    text-decoration: underline;
    text-align: center;
    font-weight: 600;
    margin: 0;
}
.subtitle-section{
    font-size: 40px;
    font-weight: 400;
    max-width: 60%;
    margin: 2rem auto;
    margin-left: 22%;
    text-align: start;
}
.middle{
    width: 100%;
    height: fit-content;
}
.wrapper_middle{
    padding: 3rem 0;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    height: fit-content;
}
.first-section{
    width: 100%;
    position: relative;
    display: flex;
    justify-content: flex-end;
    flex-direction: column;
}
.bg-overlay{
    width: 100%;
    height: 100vh;
}
.bg-overlay figure{
    display: block;
    overflow: hidden;
    outline: none;
    width: 100%;
    height: 100%;
}
.bg-overlay figure img{
    object-fit: cover;
    object-position: center;
    width: 70%;
}
.tile-on-section{
    font-size: 100px;
    font-weight: 900;
    letter-spacing: 10px;
    text-transform: uppercase;
    display: block;
    z-index: 10;
    color: white;
    text-shadow: rgb(16, 16, 16) 2px 0px 0px, rgb(16, 16, 16) 1.75517px 0.958851px 0px, rgb(16, 16, 16) 1.0806px 1.68294px 0px, rgb(16, 16, 16) 0.141474px 1.99499px 0px, rgb(16, 16, 16) -0.832294px 1.81859px 0px, rgb(16, 16, 16) -1.60229px 1.19694px 0px, rgb(16, 16, 16) -1.97998px 0.28224px 0px, rgb(16, 16, 16) -1.87291px -0.701566px 0px, rgb(16, 16, 16) -1.30729px -1.5136px 0px, rgb(16, 16, 16) -0.421592px -1.95506px 0px, rgb(16, 16, 16) 0.567324px -1.91785px 0px, rgb(16, 16, 16) 1.41734px -1.41108px 0px, rgb(16, 16, 16) 1.92034px -0.558831px 0px;
    margin: 0;
    margin-top: -4rem;
}
.subtile-on-section{
    font-size: 60px;
    font-weight: 600;
    position: relative;
    margin: 0;
}
.subtile-on-section::after{
    position: absolute;
    top: 55%;
    left: 0;
    right: 0;
    content: "";
    width: 500px;
    height: 3px;
    background-color: black;
    margin: 0 auto;
}
.on-section-actions{
    width: 70%;
    height: fit-content;
    margin: 2rem auto;
    display: flex;
    justify-content: stretch;
    align-items: center;
}
.describe-section{
    width: 70%;
    line-height: 2rem;
    font-size: 24px;
}
.buttons-action-section{
    width: 30%;
}
.buttons-action-section .btn{
    display: block;
    margin: 10px auto;
    width: 80%;
    padding: 0.55rem 0;
    border-radius: 10px;  
    cursor: pointer;  
    transition: 300ms all ease-in-out;
    color: black;
    font-weight: bold;
    font-size: 16px;
}
.prp-btn{
    background-color: white;    
    border: 1px solid black;
}
.prp-btn:hover{   
    background-color: gray;   
    color: white; 
}
.snd-btn{
    border: none;
    background-color: transparent;
}
.snd-btn:hover{
    opacity: 0.25;
}
</style>