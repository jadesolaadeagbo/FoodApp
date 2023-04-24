<template>
    <div>
      <div class="flex justify-between items-center">
        <span style="width: 40%;" class="pl-20">
          <p class="text-5xl font-bold leading-normal text-green-500" >Order Tasty and Fresh Food anytime</p>
          <p>We are the best food delivery partners for your shops and restaurants, deliver safely and on time</p>
        </span>
        <img src="../assets/hamburger.png" alt="" style="width: 50%;"/>
     </div>
     <div>             
      <p class="text-4xl font-bold pb-10">The most popular diets</p>
      
      <div class="flex flex-wrap">
        <div v-for="diet in listDiets" v-bind:key="diet.id" class="w-1/4 pb-10 p-5">
          <img v-bind:src="diet.image" class="rounded-3xl w-full" alt="" />
          <p class="font-bold text-2xl">{{diet.title}}</p>
          <span class="flex justify-between items-center pt-3">
            <p>{{diet.calories}} calories/day</p>
            <button class="bg-green-500 text-white py-2 px-3 rounded-xl">Choose</button>
          </span>

        </div>        
      </div>

     </div>


    </div>

</template>

<script>
export default{
  data(){
    return{
      listDiets:[]
    }
  },
  methods: {
    async getData(){
      const res = await fetch("https://api.spoonacular.com/recipes/findByNutrients?apiKey=d92edff2aa2e4502ad74a8cc09450343&minFat=10");
      const finalRes = await res.json();
      console.log(finalRes);
      this.listDiets = finalRes;
    
    }
  },
  mounted() {
    this.getData();
  }

}
</script>