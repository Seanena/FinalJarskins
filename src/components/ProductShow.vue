<script setup>

</script>

<template>
  <div id="myCarousel" class="carousel slide mb-6" data-bs-ride="carousel">
    <div class="carousel-indicators">
      <button type="button" data-bs-target="#myCarousel" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
      <button type="button" data-bs-target="#myCarousel" data-bs-slide-to="1" aria-label="Slide 2"></button>
      <button type="button" data-bs-target="#myCarousel" data-bs-slide-to="2" aria-label="Slide 3"></button>
    </div>
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img src="https://asset.cs2go.com/project-assets/20230912/13bfa1cc3c2daa668b6565d9fda48202.webp" style="width: 100%; height: auto; object-fit: fill; object-position: center;">
        <svg class="bd-placeholder-img" width="100%" height="100%" xmlns="http://www.w3.org/2000/svg" aria-hidden="true" preserveAspectRatio="xMidYMid slice" focusable="false"><rect width="100%" height="100%" fill="var(--bs-secondary-color)"/></svg>
        <div class="container">
        </div>
      </div>
      <div class="carousel-item">
        <img src="https://asset.cs2go.com/project-assets/20230912/0c52906e28616563f9b5cc180346c42b.webp" style="width: 100%; height:auto; object-fit: fill; object-position: center">
        <svg class="bd-placeholder-img" width="100%" height="100%" xmlns="http://www.w3.org/2000/svg" aria-hidden="true" preserveAspectRatio="xMidYMid slice" focusable="false"><rect width="100%" height="100%" fill="var(--bs-secondary-color)"/></svg>
        <div class="container">
        </div>
      </div>
      <div class="carousel-item">
        <img src="https://asset.cs2go.com/project-assets/20230912/40f5ec6b38ce0816452549d345300d4d.webp" style="width: 100%; height: auto;  object-fit: fill; object-position: center;">
        <svg class="bd-placeholder-img" width="100%" height="100%" xmlns="http://www.w3.org/2000/svg" aria-hidden="true" preserveAspectRatio="xMidYMid slice" focusable="false"><rect width="100%" height="100%" fill="var(--bs-secondary-color)"/></svg>
        <div class="container">
        </div>
      </div>
    </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#myCarousel" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#myCarousel" data-bs-slide="next">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>

  <div>
    <div class="grid-preview">
        <div class="text-preview-left">
            <h1 class="title-name-preview">Music Class</h1>
            <h4 class="detail-text-preview">"Unlock your musical potential with our Music Courses!"</h4>
        </div>
        <div class="pic-preview-right">
            <img class="pic-res-right" src="https://cdnhell.com/hellcase/img/case/obsidian_enigma/secondary_300x300.png" width="500" height="620" style="object-fit: cover;" >
        </div>
    </div> <br>
    <hr class="line">
    <div class="grid-preview">
        <div class="pic-preview">
            <img class="pic-res-left"  src="https://media.discordapp.net/attachments/1003582679465345034/1162055256750956654/da7ogam-f1defc35-83db-4319-9d8b-15117bcc3c94.png?ex=653a8b4b&is=6528164b&hm=f8f6a29ea649e507ff2abdb72f9d56cf5d4dd22db2edaaf5da7b5129b15fd266&=" width="500" height="620" style="object-fit: cover;">
        </div>
        <div class="text-preview-right">
            <h1 class="title-name-preview">Cooking Class</h1>
            <h4 class="detail-text-preview">"Discover the art of culinary delights with our Cooking Courses!"</h4>
        </div>
    </div> <br>
    <hr class="line">
    <div class="grid-preview">
        <div class="text-preview-left">
            <h1 class="title-name-preview">Drawing Class</h1>
            <h4 class="detail-text-preview">"Unleash your creativity with our Drawing Courses!"</h4>
        </div>
        <div class="pic-preview">
            <img class="pic-res-right"  src="https://scontent.fbkk12-1.fna.fbcdn.net/v/t1.15752-9/387563060_194669096981130_9094201529893012578_n.png?_nc_cat=102&ccb=1-7&_nc_sid=ae9488&_nc_eui2=AeF92bj0h4eTb4crD4xh6WZtF2Z-bTJlmugXZn5tMmWa6Bf-LSpsgzr1PTAL9AU_M8aYpO1Ekt8IbB5RjjO72_X4&_nc_ohc=b_h7Q2lXYJ0AX-46YUJ&_nc_ht=scontent.fbkk12-1.fna&_nc_e2o=s&oh=03_AdRUavb7mbaeIu81fjL-kzHAItMjD4yJnZ9gajP330xxMQ&oe=65490996" width="450" height="620" style="object-fit: cover;">
        </div>
    </div> <br> <!-- https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/4832572f-99af-4762-8892-010000fd8707/de1v51g-2ebeb7e7-0055-4972-9c31-c071d768b520.png?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcLzQ4MzI1NzJmLTk5YWYtNDc2Mi04ODkyLTAxMDAwMGZkODcwN1wvZGUxdjUxZy0yZWJlYjdlNy0wMDU1LTQ5NzItOWMzMS1jMDcxZDc2OGI1MjAucG5nIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.IzPCeRvKlcxfHpizYEvkOyUZaZuygjYILizCm-9mLAw -->
    <hr class="line">
    <div class="grid-preview">
        <div class="pic-preview">
            <img class="pic-res-left" src="https://scontent.fbkk12-1.fna.fbcdn.net/v/t1.15752-9/387329606_708111248009036_3920970528619625927_n.png?_nc_cat=111&ccb=1-7&_nc_sid=ae9488&_nc_eui2=AeElvxbui2J3fkzMKhDC6J1FWX-brOYqPuFZf5us5io-4ch2Z12atigcwUUSstWDVeL0LMBEAcMD1UrjUwKJiqZc&_nc_ohc=qjzi4IaH1GYAX8c5-wc&_nc_ht=scontent.fbkk12-1.fna&_nc_e2o=s&oh=03_AdQRUDfAXK0RQ_MSSaUDRyOhgy1KBbYryxqvvPPW6zyheg&oe=654914EE" width="500" height="550" style="object-fit: cover;">
        </div>
        <div class="text-preview-right">
            <h1 class="title-name-preview">Exercise Class</h1>
            <h4 class="detail-text-preview">"Get active and stay healthy with our Exercise Courses!"</h4>
        </div>
    </div> <br>
</div> <br> 
    
</template>


<style scoped>
body{
  margin: 0%;
  padding: 0%;
  background-color: transparent;

}

.carousel {
  margin-top: -25px;
  margin-bottom: 4rem;
}
/* Since positioning the image, we need to help out the caption */
.carousel-caption {
  bottom: 3rem;
  z-index: 10;
}

/* Declare heights because of positioning of img element */
.carousel-item {
  height: 30rem;
}

.carousel-inner {
  margin-top: 1%;
}


.marketing .col-lg-4 {
  margin-bottom: 1.5rem;
  text-align: center;
}
/* rtl:begin:ignore */
.marketing .col-lg-4 p {
  margin-right: .75rem;
  margin-left: .75rem;
}
/* rtl:end:ignore */


/* Featurettes
------------------------- */

.featurette-divider {
  margin: 5rem 0; 
}

.featurette-heading {
  letter-spacing: -.05rem;
}

/* rtl:end:remove */

/* RESPONSIVE CSS
-------------------------------------------------- */

@media (min-width: 40em) {
  .carousel-caption p {
    margin-bottom: 1.25rem;
    font-size: 1.25rem;
    line-height: 1.4;
  }

  .featurette-heading {
    font-size: 50px;
  }
}

@media (min-width: 62em) {
  .featurette-heading {
    margin-top: 7rem;
  }
}

.cardframe:hover{
  box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.2);
}
.panelbuttcon{
  display: flex;
}

.buttcon{
  display: flex;
  margin: auto;
  justify-content: space-between;
  align-items: center;
  width: 70%;
  
}

.indisbutt{
  margin: auto;
}

.quatitybuttbgminus:hover{
background-color: rgb(248, 79, 49);
}

.quatitybuttbgplus:hover{
background-color: rgb(35, 197, 82);
}


.quatitybutt{
  border: hidden;   
  background-color: transparent;
}

.no-spinners::-webkit-inner-spin-button,
.no-spinners::-webkit-outer-spin-button {
  -webkit-appearance: none;
  appearance: none;
  margin: 0; 
}


.imgbutt{
  width: 1vw;
}

.addtocartbutt{
    background-color: rgb(255, 172, 47);
    border: hidden;
  }

  .addtocartbutt:hover{
    background-color: rgb(207, 130, 13);
    border: hidden;
  }

  .homepagebutt{
    background-color: rgb(168, 23, 15);
    border: hidden;
  }

  .homepagebutt:hover{
    background-color: rgb(119, 14, 8);
    border: hidden;
  }

.modal {
    display: none;
    position: fixed;
    z-index: 1;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(148, 148, 148, 0.5);
}

@media screen and (max-width: 700px) {
  .carouselcon{
    width: 90%;
    border: hidden  rgb(255, 189, 42);
    
  }

  .carouselIMG{
    border: 4px solid rgb(90, 5, 0);
    border-radius: 5px;
  }

  .imgbutt{
  width: 5vw;
}

  .modal-content{
    width: 95vw;
    position: relative;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: rgb(255, 255, 255);
    background-color: rgb(100, 20, 20);
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    text-align: center;
 }
 .modal-content h3{
    padding: 0%;
    font-weight: 600;
    margin-bottom: 1%;
 }

 .modal-content p {
    font-size: 16px;
    font-weight: 600;
    padding: 0%;
    margin-bottom: 1%;
 }

 .modal-content marquee{
    font-size: 16px;
    font-weight: 700;
    padding: 0%;
    
 }


}

@media screen and (min-width: 768px) {
  .carouselcon{
    width: 70%;
    border: hidden  rgb(255, 189, 42);
    
  }

  .carouselIMG{
    border: 5px solid  rgb(90, 5, 0);
    border-radius: 5px;
  }
  .imgbutt{
  width: 2vw;
}
  .modal-content {
    width: 70dvw;
    position: relative;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: rgb(255, 255, 255);
    background-color: rgb(100, 20, 20);
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    text-align: center;
 }
 .modal-content h3{
    padding: 0%;
    font-weight: 600;
    margin-bottom: 1%;
 }

 .modal-content p {
    font-size: 16px;
    font-weight: 600;
    padding: 0%;
    margin-bottom: 1%;
 }

 .modal-content marquee{
    font-size: 16px;
    font-weight: 700;
    padding: 0%;
    
 }
}

@media screen and (min-width: 1024px) {
  .carouselcon{
    width: 70%;
    border: hidden  rgb(255, 189, 42);
    
  }

  .carouselIMG{
    border: 8px solid  rgb(90, 5, 0);
    border-radius: 7px;
  }
  .imgbutt{
  width: 2vw;
}
  .modal-content {
    width: 70vw;
    position: relative;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: rgb(255, 255, 255);
    background-color: rgb(100, 20, 20);
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    text-align: center;
 }
 .modal-content h3{
    padding: 0%;
    font-weight: 600;
    margin-bottom: 1%;
 }

 .modal-content p {
    font-size: 16px;
    font-weight: 700;
    padding: 0%;
    margin-bottom: 1%;
 }

 .modal-content marquee{
    font-size: 16px;
    font-weight: 700;
    padding: 0%;
    
 }
}

@media screen and (min-width: 1440px) {
  .carouselcon{
    width: 60%;
    border: hidden  rgb(255, 189, 42);
    
  }

  .carouselIMG{
    border: 8px solid  rgb(90, 5, 0);
    border-radius: 10px;
  }
  .imgbutt{
  width: 1vw;
}
  .modal-content {
    width: 70vw;
    position: relative;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: rgb(255, 255, 255);
    background-color: rgb(100, 20, 20);
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    text-align: center;
 }
 .modal-content h3{
    padding: 0%;
    font-weight: 600;
    margin-bottom: 1%;
 }

 .modal-content p {
    font-size: 20px;
    font-weight: 700;
    padding: 0%;
    margin-bottom: 1%;
 }

 .modal-content marquee{
    font-size: 16px;
    font-weight: 700;
    padding: 0%;
    
 }
}


.close {
    position: absolute;
    top: 5px;
    right: 10px;
    font-size: 24px;
    font-weight: bold;
    cursor: pointer;
}


.close:hover {
    color: red;
}

.title-name-preview{
    color: #ffa601;
}
.detail-text-preview{
    color: var(--secondary-color)
}
.pic-res-left{
    transition: 1s;
    margin-right: -5rem;

}
.pic-res-right{
    transition: 1s;
    margin-left: -5rem;
}
.grid-preview{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    justify-content: center;
    justify-items:  center;
    transition: 1.6s;
    margin: 2rem -10rem;
}
.grid-preview:hover{
    transform: scale(1.175);
}
.text-preview-left{
    text-align: center;
    margin: auto 0;
    margin-right: -15rem;
}
.text-preview-right{
    text-align: center;
    margin: auto 0;
    margin-left: -15rem;
}

@media screen and (max-width: 1690px) {
    .pic-res-left{
    transition: 1s;
    margin: 0 2rem;
}

.pic-res-right{
    transition: 1s;
    margin: 0 1.5rem;
}
.grid-preview{
    margin: 2rem -3rem;
}
.grid-preview:hover{
    transform: scale(1.125);
}
.text-preview-left{
    text-align: center;
    margin: auto 0;
    margin-right: -10rem;
}
.text-preview-right{
    text-align: center;
    margin: auto 0;
    margin-left: -10rem;
}
}
@media screen and (max-width: 1100px) {
    .grid-preview{
    margin: 2rem auto;
}
  .grid-preview:hover{
    transform: scale(1.1);
    }
    .pic-res-left{
   object-fit: cover;
   width: 80%;
   height: 100%;
    }
    .pic-res-right{
   object-fit: cover;
   width: 80%;
   height: 100%;
    }
    .text-preview-left{
    text-align: center;
    margin: auto 0;
    margin-right: auto;
}
.text-preview-right{
    text-align: center;
    margin: auto 0;
    margin-left: auto;
}
}
@media screen and (max-width: 1300px) {
.column{
    grid-template-columns: repeat(1, 1fr);
  }
  .grid-preview:hover{
    transform: scale(1.1);
    }
    .datail-text-preview{
        font-size: 1.3rem;
    }
}
@media screen and (max-width: 1000px) {
    .pic-res-left{
   object-fit: cover;
   width: 80%;
   height: 100%;
    }
    .pic-res-right{
   object-fit: cover;
   width: 80%;
   height: 100%;
    }
    .title-name-preview{
    font-size: 1.5rem;
    }
    .datail-text-preview{
    font-size: 1rem;
    }
    .grid-preview:hover{
    transform: scale(1.05);
    }
}

@keyframes grid-anime{
    0%{
        transform: scale(1);
        animation: ease-out;
    }
    50%{
        transform: scale(1.15);
        animation: ease-in;
    }
    100%{
        transform: scale(1);
    }
}




</style>