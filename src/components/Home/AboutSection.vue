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
    created () {
    window.addEventListener('scroll', this.handleScroll);
    },
    destroyed () {
        window.removeEventListener('scroll', this.handleScroll);
    },
    methods: {
        handleScroll (event) {
            console.log(event);
        }
    }
}
</script>
<style>
.about-section{
    width: 100%;
    height: fit-content;
}
.about-section .content-section{
    position: relative;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    flex-wrap: wrap;
    height: 100%;
    padding: 4rem 10px;
}
.title-section{
    width: 100%;
    max-height: 40%;
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
    height: 60vh;
    position: relative;
    display: flex;
}
.on-describe-img-section figure{
    position: relative;
    display: block;
    width: 100%;
    height: 100%;
    max-height: 90%;
    max-width: 70%;
    margin: auto;   
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
    width: 50%;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    position: relative;
    overflow: hidden;
    outline: none;
    height: 60%;
    padding-bottom: 3rem;
}
.text-section{
    font-size: 24px;
    line-height: 2rem;
    color: black;
    text-align: start;
    padding-right: 3rem;
}
@media only screen and (max-width: 1400px) {
    .title-section{
        font-size: 120px;
    }
    .on-describe-img-section{
        margin-top: 2rem;
    }
    .on-describe-img-section figure{
        height: 100%;
        width: 80%;  
    }
    .text-descrip-section{
        padding-bottom: 0rem;
    }
    .text-section{
        font-size: 20px;
    }
}
@media only screen and (max-width: 992px) {
    .title-section{
        font-size: 120px;
    }
    .title-section span{
        margin-left: 5rem;
    }
    .on-describe-img-section{
        width: 100%;        
        margin:0;
    }
    .on-describe-img-section figure{
        max-height: 80%;
        max-width: 90%;
    }
    .text-descrip-section{
        width: 100%;
        height: 50%;
    }
    .text-section{
        align-items: flex-start;
        text-align: center;
        padding: 0 10px;
    }
}
@media only screen and (max-width: 768px) {
    .title-section{
        font-size: 100px;
        margin-left: 0;
        margin-bottom: 2rem;
    }
    .title-section span{
        margin-left: 2rem;
    }
    .on-describe-img-section{
        width: 100%;
        margin:0;
    }
    .on-describe-img-section figure{
        max-height: 80%;
        max-width: 90%;
    }
    .text-descrip-section{
        width: 100%;
    }
    .text-section{
        align-items: flex-start;
        text-align: center;
        padding: 0 10px;
    }
}
@media only screen and (max-width: 576px) {
    .title-section{
        font-size: 60px;
        margin-left: 0;
        margin-bottom: 0;
    }
    .title-section span{
        margin-left: 2rem;
    }
    .on-describe-img-section{
        margin:0;
        height: 50vh;
    }
    .on-describe-img-section figure{
        width: 90%;
    }
    .text-descrip-section{
        width: 100%;
    }
    .text-section{
        font-size: 18px;
        align-items: flex-start;
        text-align: center;
        padding: 0 10px;
        line-height: 1.5rem;
    }
}
@media only screen and (max-width: 374.98px) {
    .title-section{
        font-size: 50px;
        margin-left: 0;
        margin-bottom: 0;
    }
    .title-section span{
        margin-left: 2rem;
    }
    .on-describe-img-section{
        width: 100%;
        margin:0;
    }
    .on-describe-img-section figure{
        width: 90%; 
    }
    .text-descrip-section{
        width: 100%;
        height: 55%;
    }
    .text-section{
        font-size: 14px;
        align-items: flex-start;
        text-align: center;
        padding: 0 10px;
    }
}
</style>