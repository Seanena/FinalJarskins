<script setup>
import { RouterLink } from 'vue-router';


</script>

<template>
     <header  style="background-image: url('/headerBG.png'); background-size: cover;">
        <div class="container">
            <nav class="navbar navbar-expand-lg navbar-light">
                <a href="/" class="d-flex align-items-center mb-3 mb-md-0 me-md-auto link-body-emphasis text-decoration-none" style="margin-left: 40px;">
                <img src="https://i.imgur.com/vgAVqbA.png" alt="" width="50" height="50"> &nbsp; &nbsp;
                <span class="fs-4" style="color: white;">JARSKINS</span>
            </a>
                
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation" style="border: solid 2px white;">
                    <img src="@/assets/menu.png" alt="Menu" style="width: 24px; height: 24px;">
                </button>
                <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
                    <ul class="navbar-nav">
                        <li class="nav-item">
                            <RouterLink to="/market">
                                <button class="c-button c-button--gooey"  style="margin-right: 10px;" > ร้านค้า
                                <div class="c-button__blobs">
                                <div></div>
                                <div></div>
                                <div></div>
                                </div>
                                </button>
                            </RouterLink>   
                        </li>
                        <li class="nav-item">
                            <RouterLink to="/cart">
                                <button class="c-button c-button--gooey" style="margin-right: 10px;" > ตะกร้า
                                <div class="c-button__blobs">
                                <div></div>
                                <div></div>
                                <div></div>
                                </div>
                                </button>
                            </RouterLink> 
                        </li>
                        <li class="nav-item">
                            <RouterLink to="/historyorder">
                                <button class="c-button c-button--gooey"  style="margin-right: 10px;" > ประวัติคำสั่งซื้อ
                                <div class="c-button__blobs">
                                <div></div>
                                <div></div>
                                <div></div>
                                </div>
                                </button>
                            </RouterLink>   
                        </li>
                    </ul>
                </div>
            </nav>
        </div>
    </header>

    
</template>

<style scoped>

#icon-theme{
  margin: auto 20px;
  width: 50px;
  height: 50px;
  cursor: pointer;
  transition: 1s;

}
#icon-theme:hover{
  animation-name: rotate;
  -webkit-animation: rotate 3s normal linear infinite;
  animation: rotate 3s normal linear infinite;
  scale: 1.5;
}

:root{
   --primary-color: #f4fdff;
  --secondary-color: #212121; 
}

.dark-theme{
 --primary-color: #161616;
 --secondary-color: #ffffff;
}

@keyframes rotate {
  0% {
    -webkit-transform: rotate3d(0, 0, 1, 0deg);
    transform: rotate3d(0, 0, 1, 0deg);
  }
  25% {
    -webkit-transform: rotate3d(0, 0, 1, 90deg);
    transform: rotate3d(0, 0, 1, 90deg);
  }
  50% {
    -webkit-transform: rotate3d(0, 0, 1, 180deg);
    transform: rotate3d(0, 0, 1, 180deg);
  }
  75% {
    -webkit-transform: rotate3d(0, 0, 1, 270deg);
    transform: rotate3d(0, 0, 1, 270deg);
  }
  100% {
    -webkit-transform: rotate3d(0, 0, 1, 360deg);
    transform: rotate3d(0, 0, 1, 360deg);
  }
}
/* navbar */

.navbar-ct{
  margin: 6.5rem auto;
}
.fixed-header{
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  background-color: #212121;
  z-index: 1000;
}
/*  */
.c-button {
  background-color: #212121;
  margin: 10px;
  color: #f8a9ff;
  font-weight: 700;
  font-size: 16px;
  text-decoration: none;
  padding: 0.5em 1em;
  cursor: pointer;
  display: inline-block;
  vertical-align: middle;
  position: relative;
  z-index: 1;
}

.c-button--gooey {
  color: #ffffff;
  text-transform: uppercase;
  letter-spacing: 2px;
  border: 4px solid #F5BCC6;
  border-radius: 50px;
  position: relative;
  transition: all 500ms ease;
}

.c-button--gooey .c-button__blobs {
  height: 100%;
  filter: url(#goo);
  overflow: hidden;
  position: absolute;
  top: 0;
  left: 0;
  bottom: -3px;
  right: -1px;
  z-index: -1;
  border-radius: 50px; /* ปรับ border-radius เป็นค่าที่เหมาะสมกับวงรีที่ต้องการ */
}

.c-button--gooey .c-button__blobs div {
  background-color: hsl(353, 21%, 100%);
  width: 100%;
  height: 100%;
  border-radius: 50px; /* ปรับ border-radius เป็นค่าที่เหมาะสมกับวงรีที่ต้องการ */
  position: absolute;
  transform: scale(1.4) translateY(125%) translateZ(0);
  transition: all 600ms ease;
}


.c-button--gooey .c-button__blobs div:nth-child(1) {
  left: -5%;
}

.c-button--gooey .c-button__blobs div:nth-child(2) {
  left: 30%;
  transition-delay: 60ms;
}

.c-button--gooey .c-button__blobs div:nth-child(3) {
  left: 66%;
  transition-delay: 25ms;
}

.c-button--gooey:hover {
  color: #212121;
}

.c-button--gooey:hover .c-button__blobs div {
  transform: scale(1.4) translateY(0) translateZ(0);
}
/* */
.form-control-dark {
  border-color: var(--bs-gray);
}
.form-control-dark:focus {
  border-color: #000000;
  box-shadow: 0 0 0 .25rem rgba(255, 255, 255, .25);
}
.text-small {
  font-size: 85%;
}

.dropdown-toggle:not(:focus) {
  outline: 0;
}
@media screen and (max-width: 1560px) {
  .navbar-ct{
  margin: 6.98rem auto;
}
}

@media screen and (max-width: 560px) {
  .fs-4{
    margin-right: 200px;
  }
  .navbar-ct{
  margin: 12.2rem auto;
}
}
@media screen and (max-width: 445px) {
  .fs-4{
    margin-right: 100px;
  }
  .navbar-ct{
  margin: 10.3rem auto;
}
.c-button--gooey{
  margin-top: -20px;
}
#icon-theme{
  margin: auto 20px;
  margin-top: -20px ;
}
}

</style>
