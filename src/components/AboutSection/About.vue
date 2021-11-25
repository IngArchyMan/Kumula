<template>
    <div class="about-section">
        <div class="content-section">
            <h1 class="title-section">HEADER <br> <span>TITLE ONE</span></h1>
            <div class="on-describe-img-section">
                <figure>
                    <img src="@/assets/img/about-img-section.jpg" alt="About Us img" class="section-prp-img">
                </figure>
            </div>
            <div class="text-descrip-section">
                <p class="text-section">Lorem ipsum dolor sit amet consectetur adipisicing elit. Corrupti suscipit unde similique reiciendis eligendi a tempora veniam non quis reprehenderit, magnam quos hic fugit aspernatur officia incidunt cupiditate quibusdam sapiente!
                Voluptates officia laboriosam deserunt doloremque, odio similique reiciendis molestias temporibus nisi aut officiis quis veritatis quam! In cum dicta tempore ipsa perferendis hic, sint necessitatibus aliquam consequatur molestias nemo voluptas.</p>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'About', 
}
</script>
<style>
.about-section{
    width: 100%;
    height: 100vh;
    padding: 5rem 10px;
}
.about-section .content-section{
    position: relative;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    flex-wrap: wrap;
}
.title-section{
    width: 100%;
    font-size: 150px;
    text-align: start;
    margin: 0;
    margin-left: 6rem;
}
.title-section span{
    margin-left: 20rem;
}
.on-describe-img-section{
    width: 50%;
    position: relative;
    margin-left: 5rem;
}
.on-describe-img-section figure{
    position: relative;
    display: block;
    width:  100%;
    height: 40rem;
    margin: 0;   
}
.on-describe-img-section figure::after{
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    content: "";
    width: 90%;
    height: 90%;
    border: 5px solid #2F4858;
    border-radius: 20px;
    margin: auto;
}
.on-describe-img-section figure img{
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    width: 100%;
    height: 100%;
    border-radius: 20px;
    box-shadow: 0px 0px 14px 3px rgba(66,66,66,0.68);
}
.text-descrip-section{
    width: 40%;
    display: flex;
    align-items: center;
    position: relative;
    overflow: hidden;
    outline: none;
    height: 50rem;
}
.text-section{
    font-size: 24px;
    line-height: 2rem;
    color: black;
    text-align: start;
    padding-right: 1rem;
    padding-left: 3rem;
}
</style>