<script setup>
import { RouterLink } from 'vue-router';
import  { useProductStore } from '@/stores/products'
const storeProduct = useProductStore()

const addToCart = (productData) => {
  storeProduct.addToCart({
    id: productData.id,
    Name: productData.Name,
    Price: productData.Price,
    PriceCal: productData.PriceCal,
    img: productData.img,
    quatity: productData.quatity,
  });
};

</script>

<template>
    
    <div class="row row-cols-1 row-cols-md-2 row-cols-lg-3 row-cols-xl-5 mt-3" style="width: 95%; margin: auto;">
      <div class="col mb-4" v-for="(productData, index) in storeProduct.productsList" :key="index">
        <div class="card cardframe" style="border-radius: 0%; border: hidden;">
          <img :src="productData.img" class="card-img-top" alt="productImg" style="border-radius: 0%;">
          <div class="card-body">
            <h6 class="card-title mt-3" style=" color: rgb(11, 34, 57);">{{ productData.Name }}</h6>
            <div class="pricetag">
                <p style="  color: rgb(11, 34, 57);">{{ productData.Price }}</p>
              </div>
          
            
            <div class="panelbuttcon">
              <button type="button" class="btn btn-success addtocartbutt" style="margin: auto; margin-bottom: 1%; width: 100%;"  @click="addToCart(productData)">เพิ่ม</button>
            </div>
          </div>
        </div>
      </div>
    </div>

  
    
</template>