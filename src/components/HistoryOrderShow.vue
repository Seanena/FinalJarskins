<script setup>
import  { useProductStore } from '@/stores/products'
const storeProduct = useProductStore()


function formatNumberWithCommas(number) {
    const formattedNumber = Number(number).toFixed(2);
    return formattedNumber.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
}

function formatNumberWithCommasonly(number) {
  return number.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ',');
}


</script>

<template>
    <div v-if="storeProduct.OrderList.length > 0" class="outcon">

        <div class="incomplete" style="width: 100%;">
              <div class="container-xl mt-3" style="background-color: #333; height: 40px; border-radius: 5px; width: 90%;">
              <table style="background-color: #333; text-align: center vertical-align:middle;">
                <thead class="top">
                  <RouterLink to="/cart">
                    <a href="" style="margin-right: 20px;">cart</a>
                  </RouterLink>
                  <RouterLink to="/historyorder">
                    <a href="" style="color: red;">history</a>
                  </RouterLink>
                </thead>
            </table>
              </div>
            <div class="lateorder  mb-5 mt-2" v-for="(order, index) in storeProduct.OrderList" :key="index" style="background-color: #333; width: 90%; margin:0 auto;">
                <div class="orderdetail table-container">
                    <table class="table"  style="text-align: center; vertical-align: middle; background-color: #333;">
                    <thead class="thead-light">
                      <tr>
                        <th scope="col" style="width:15%;">ข้อมูลคำสั่งซื้อ</th>
                        <th scope="col" style="width:55%;">ข้อมูลสกิน</th>
                        <th scope="col" style="width:15%;">ราคาซื้อ</th>
                        <th scope="col" style="width:15%;">ผู้ซื้อ</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="(product, Index) in order.CartList" :key="Index">
                        <td class="product-grid">
                            <div class="product-image">
                            <img :src="product.img" alt="" style="border-radius: 10px; width: 70%;">
                            </div>
                            <div class="product-name">
                            <span>{{ product.Name }}</span>
                            </div>
                        </td>
                        <td>{{ product.Price }}</td>
                        <td>
                            {{ formatNumberWithCommasonly(product.quatity) }} 
                        </td>
                        <td>{{ formatNumberWithCommas(product.totalProductPrice) }}</td>
                        </tr>
                    </tbody>
                    </table>
                    <div class="priceshow" style="color: white;">
                        <p>รวม : {{ formatNumberWithCommas(order.Total) }} บาท</p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div v-else class="outcon">
      <div class="incomplete" style="width: 100%;">
              <div class="container-xl mt-3" style="background-color: #333; height: 40px; border-radius: 5px; width: 90%;">
              <table style="background-color: #333; text-align: center vertical-align:middle;">
                <thead class="top">
                  <RouterLink to="/cart">
                    <a href="" style="margin-right: 20px;">cart</a>
                  </RouterLink>
                  <RouterLink to="/historyorder">
                    <a href="" style="color: red;">history</a>
                  </RouterLink>
                </thead>
            </table>
              </div>
      <div class="outcon" style="width: 90%; margin: 0 auto;">
            <div class="container-xl mt-2" style="background-color: #333; border-radius: 10px; height: 200px;">
                <div class="bd-example table-container ">
                <table class="table"  style="text-align: center; vertical-align: middle;">
                    <thead class="thead-dark">
                    <tr>
                    <th scope="col" style="width:40%; background-color: #333; color: #d9d9d9;">ข้อมูลสินค้า</th>
                    <th scope="col" style="width:10%; background-color: #333; color:#d9d9d9;">ราคา</th>
                    <th scope="col" style="width:10%; background-color: #333;color:#d9d9d9;">วิธีชำระเงิน</th>
                    <th scope="col" style="width:20%; background-color: #333;color:#d9d9d9;">สถานะ</th>
                    </tr>
                </thead>
                <br>
                <tbody style="color: #333;">
                    <tr v-for="(productData, index) in storeProduct.CartList" :key="index">
                    <td>
                        <div class="product-grid">
                        <div class="product-image">
                        <img :src="productData.img" alt="" style="width: 70%;">
                        </div>
                        <div class="product-name">
                        <span>{{ productData.Name }}</span>
                        </div>
                        </div>
                    </td>
                    <td>{{ productData.Price }}</td>
                    <td>Promtpay</td>
                    <td>
                        <button class="btn btn-danger" @click="removeFromCart(productData.id)" style="width: 60%; background-color: red; color: white;">
                            DELETE
                        </button>
                    </td>
                    </tr>
                    
                </tbody>

                </table>
                </div>
            </div>
        </div>       
      </div>
    </div>


</template>


<style scoped>

a{
  font-size: 25px;
  text-decoration: none;
  color: #d9d9d9;
}

.lateorder{
    padding: 1%;
    background-color: rgb(255, 255, 255);
    border-radius: 10px;
}

.orderdetailhead{
    color: rgb(89, 24, 20);
    text-align: center;
}

.customerDetail{
    margin-left: 2%;
    font-size: large;
    color: rgb(89, 24, 20);
}

.priceshow{
    margin-right: 2%;
    text-align: right;
    font-size: large;
    color: rgb(89, 24, 20);
}

.outcon{
    display: flex;
    
}

.maincontainerr{
    border-radius: 10px;
    padding:1%;
    width: 90%;
    margin: auto;
    background-color: rgb(89, 24, 20);
}

.cartheadd{
    text-align: center;
    margin-bottom: 2%;
    color: rgb(255, 255, 255);
}

.table td {
    padding: 0.2rem;
}

.product-grid {
  display: grid;
  grid-template-columns: 30% 70%;
  grid-column-gap: 2%; 
  align-items: center; 
}

.custom-table {
  background-color: rgb(240, 240, 240); 
  
}

.custom-table th {
  background-color: rgb(89, 24, 20); 
  color: rgb(255, 255, 255); 
}

.custom-table td {
  background-color: rgb(245, 245, 245); 
  color: #333; 
  border: 1px solid rgb(230, 221, 221);
   
}

.binbutt{
  border-radius: 10px;
  padding: 2%;
  border: hidden;   
  background-color: transparent;
  background-color: rgb(255, 255, 255);
}

.binbutt:hover{
  border: hidden;   
  background-color: rgb(248, 79, 49);
}


.maincontainerrnull{
    border-radius: 10px;
    padding:1%;
    width: 90%;
    margin: auto;
    background-color: rgb(89, 24, 20);
}

.lateordernull{
    padding: 1%;
    background-color: rgb(255, 255, 255);
    border-radius: 10px;
}


.orderdetailheadnull h4{
    color: rgb(89, 24, 20);;
    text-align: center;
    padding-top: 25vh;
    padding-bottom: 25vh;
}

@media screen and (max-width: 700px) {
.customerDetail{
    margin-left: 2%;
    font-size:small;
    color: rgb(89, 24, 20);
}

.orderdetailhead{
    margin-top: 2%;
    color: rgb(89, 24, 20);
    text-align: center;
}
.outcon{
    display: flex;
    
}
.outconbill{
    display: flex;
    margin-bottom: 2%;
}

.maincontainer{
    border-radius: 10px;
    padding:1%;
    width: 90%;
    margin: auto;
    background-color: white;
}

.mainbillcontainer{
    border-radius: 10px;
    padding:1%;
    width: 90%;
    margin-left: 5%;
    background-color: white;
}

.carthead{
    text-align: center;
    margin-bottom: 2%;
    color: rgb(95, 20, 17);
}

.billhead{
    color: rgb(95, 20, 17);
    text-align: center;
}

.detailbill{
    color: rgb(95, 20, 17);
    text-align:left;
    font-size: larger;
}

.table td {
    padding: 0.2rem;
}

.product-grid { 
  display: grid;
  grid-template-columns: 0% 100%;
  grid-column-gap: 2%; 
  align-items: center; 
}

.product-image{
    display: none;
}

.imgbutt{
  width: 1vw;
}

.buttcon{
  display: flex;
  margin: auto;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  
}

.no-spinners::-webkit-inner-spin-button,
.no-spinners::-webkit-outer-spin-button {
  -webkit-appearance: none;
  appearance: none;
  margin: 0;
}

.quatitybuttbgminus{
    display: none;
    width: 2.3rem;
}

.quatitybuttbgplus{
    display: none;
    width: 2.3rem;
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

.table-container {
  overflow-x: auto;
  max-width: 100%; 
  margin: 0 auto; 
}

.custom-table {
  background-color: rgb(240, 240, 240); 
  border-collapse: collapse; 
  
}


.custom-table th {
  background-color:rgb(95, 20, 17) ; 
  color: rgb(255, 255, 255); 
}


.custom-table td {
  background-color: rgb(236, 236, 236); 
  color: rgb(95, 20, 17); 
  border: 1px solid rgb(230, 221, 221);
   
}


.binbutt{
  border-radius: 10px;
  padding: 2%;
  border: hidden;   
  background-color: transparent;
  background-color: rgb(255, 255, 255);
  color: rgb(95, 20, 17);
}

.binbutt:hover{
  border: hidden;   
  background-color: rgb(248, 79, 49);
}

.panelbuttcon{
    display: flex;
}

}

@media screen and (min-width: 768px) {
.customerDetail{
    margin-left: 2%;
    font-size:medium;
    color: rgb(89, 24, 20);
}

.orderdetailhead{
    margin-top: 1%;
    color: rgb(89, 24, 20);
    text-align: center;
}
.outcon{
    display: flex;
    
}
.outconbill{
    display: flex;
    margin-bottom: 2%;
}

.maincontainer{
    border-radius: 10px;
    padding:1%;
    width: 90%;
    margin: auto;
    background-color: white;
}

.mainbillcontainer{
    border-radius: 10px;
    padding:1%;
    width: 60%;
    margin-left: 35%;
    background-color: white;
}

.carthead{
    text-align: center;
    margin-bottom: 2%;
    color: rgb(95, 20, 17);
}

.billhead{
    color: rgb(95, 20, 17);
    text-align: center;
}

.detailbill{
    color: rgb(95, 20, 17);
    text-align:left;
    font-size: larger;
}

.table td {
    padding: 0.2rem;
}

.product-grid { 
  display: grid;
  grid-template-columns: 30% 70%;
  grid-column-gap: 2%; 
  align-items: center; 
}

.imgbutt{
  width: 1vw;
}

.buttcon{
  display: flex;
  margin: auto;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  
}

.no-spinners::-webkit-inner-spin-button,
.no-spinners::-webkit-outer-spin-button {
  -webkit-appearance: none;
  appearance: none;
  margin: 0;
}

.quatitybuttbgminus{
    width: 2.3rem;
}

.quatitybuttbgplus{
    width: 2.3rem;
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


.custom-table {
  background-color: rgb(240, 240, 240); 
  border-collapse: collapse; 
  
}


.custom-table th {
  background-color:rgb(95, 20, 17) ; 
  color: rgb(255, 255, 255); 
}


.custom-table td {
  background-color: rgb(236, 236, 236); 
  color: rgb(95, 20, 17); 
  border: 1px solid rgb(230, 221, 221);
   
}


.binbutt{
  border-radius: 10px;
  padding: 2%;
  border: hidden;   
  background-color: transparent;
  background-color: rgb(255, 255, 255);
  color: rgb(95, 20, 17);
}

.binbutt:hover{
  border: hidden;   
  background-color: rgb(248, 79, 49);
}

.panelbuttcon{
    display: flex;
}

}

@media screen and (min-width: 1024px) {
.customerDetail{
    margin-left: 2%;
    font-size: large;
    color: rgb(89, 24, 20);
}

.reorderbutt{
    margin-top: 12vh;
}
.outcon{
    display: flex;
    
}
.outconbill{
    display: flex;
    margin-bottom: 2%;
}

.maincontainer{
    border-radius: 10px;
    padding:1%;
    width: 90%;
    margin: auto;
    background-color: white;
}

.mainbillcontainer{
    border-radius: 10px;
    padding:1%;
    width: 50%;
    margin-left: 45%;
    background-color: white;
}

.carthead{
    text-align: center;
    margin-bottom: 2%;
    color: rgb(95, 20, 17);
}

.billhead{
    color: rgb(95, 20, 17);
    text-align: center;
}

.detailbill{
    color: rgb(95, 20, 17);
    text-align:left;
    font-size: larger;
}

.table td {
    padding: 0.2rem;
}

.product-grid {
  display: grid;
  grid-template-columns: 30% 70%;
  grid-column-gap: 2%; 
  align-items: center; 
}

.imgbutt{
  width: 1vw;
}

.buttcon{
  display: flex;
  margin: auto;
  justify-content: space-between;
  align-items: center;
  width: 80%;
  
}

.no-spinners::-webkit-inner-spin-button,
.no-spinners::-webkit-outer-spin-button {
  -webkit-appearance: none;
  appearance: none;
  margin: 0;
}

.quatitybuttbgminus{
    width: 3rem;
}

.quatitybuttbgplus{
    width: 3rem;
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


.custom-table {
  background-color: rgb(240, 240, 240); 
  border-collapse: collapse; 
  
}


.custom-table th {
  background-color: rgb(95, 20, 17); 
  color: rgb(255, 255, 255); 
}


.custom-table td {
  background-color: rgb(236, 236, 236); 
  color: #333; 
  border: 1px solid rgb(230, 221, 221);
   
}


.binbutt{
  border-radius: 10px;
  padding: 2%;
  border: hidden;   
  background-color: transparent;
  background-color: rgb(255, 255, 255);
}

.binbutt:hover{
  border: hidden;   
  background-color: rgb(248, 79, 49);
}

.panelbuttcon{
    display: flex;
}

}

@media screen and (min-width: 1300px) {
    .outcon{
    display: flex;
    
}
.outconbill{
    display: flex;
    margin-bottom: 2%;
}

.maincontainer{
    border-radius: 10px;
    padding:1%;
    width: 90%;
    margin: auto;
    background-color: white;
}

.mainbillcontainer{
    border-radius: 10px;
    padding:1%;
    width: 30%;
    margin-left: 65%;
    background-color: white;
}

.carthead{
    text-align: center;
    margin-bottom: 2%;
    color: rgb(95, 20, 17);
}

.billhead{
    color: rgb(95, 20, 17);
    text-align: center;
}

.detailbill{
    color: rgb(95, 20, 17);
    text-align:left;
    font-size: larger;
}

.table td {
    padding: 0.2rem;
}

.product-grid {
  display: grid;
  grid-template-columns: 30% 70%;
  grid-column-gap: 2%; 
  align-items: center; 
}

.imgbutt{
  width: 1vw;
}

.buttcon{
  display: flex;
  margin: auto;
  justify-content: space-between;
  align-items: center;
  width: 70%;
  
}

.no-spinners::-webkit-inner-spin-button,
.no-spinners::-webkit-outer-spin-button {
  -webkit-appearance: none;
  appearance: none;
  margin: 0;
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


.custom-table {
  background-color: rgb(240, 240, 240); 
  border-collapse: collapse; 
  
}


.custom-table th {
  background-color: rgb(95, 20, 17); 
  color: rgb(255, 255, 255); 
}


.custom-table td {
  background-color: rgb(236, 236, 236); 
  color: rgb(95, 20, 17); 
  border: 1px solid rgb(230, 221, 221);
   
}


.binbutt{
  border-radius: 10px;
  padding: 2%;
  border: hidden;   
  background-color: transparent;
  background-color: rgb(255, 255, 255);
}

.binbutt:hover{
  border: hidden;   
  background-color: rgb(248, 79, 49);
}

.panelbuttcon{
    display: flex;
}

}

</style>
