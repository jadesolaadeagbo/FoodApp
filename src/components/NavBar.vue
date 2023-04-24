<template>
    <div class="flex px-20 justify-between items-center p-10">
        <div class="logo flex justify-between space-x-2 items-center">
            <img src="../assets/Subtract.svg" alt="">
            <p class="text-2xl font-bold">FitMe</p>            
        </div>

            <div class="flex items-center space-x-10">
                <!-- <i class="fa fa-bars lg:hidden" aria-hidden="true" ></i> -->
                <ul class="flex items-center space-x-10">
                    <li><a href="#">DIETS</a></li>
                    <li><a href="#">CALORIE CALCULATOR</a></li>
                    <li><a href="#">MENU</a></li>
                    <li><a href="#">DELIVERY</a></li>
                    <li><a href="#">ABOUT US</a></li>
                    <LI><a href="#">BLOG</a></LI>
                    <LI><a href="#">FAQ</a></LI>
                </ul>      
            </div>




        <div class="flex space-x-5">
            <img src="../assets/Bag.svg" alt="">
            <button class="bg-black text-white rounded-2xl py-2 px-5">Sign in</button>
        </div>
       

    </div>
  </template>
  
  <script>
  export default{
    data(){
        return{
            isOpen: false,
        }
        
    }
  }
  </script>
  
  <style>
  
  </style>