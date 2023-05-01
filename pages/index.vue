


<template>
     

    <!-- Create By Joker Banny -->
    
<body  class="bg-white">



<!-- Title -->
 

<!-- Tab Menu -->
<div class="flex flex-wrap items-center  overflow-x-auto overflow-y-hidden py-10 justify-center   bg-white text-gray-800">
	 
</div>

<!-- Product List -->
<section class="py-10 bg-gray-100">
   <div class="mx-auto grid max-w-6xl  grid-cols-1 gap-6 p-6 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4">
    
    <div v-for="p in prod">
        
    <Card :id="p.id" :title="p.title" :price="p.price" :category="p.category" :description="p.description" :image="p.image"/>
    </div> 


</div>
 
</section>



  
</body>
 </template>


<script setup>
const config = useRuntimeConfig()
const {data: prod} = await useFetch('https://fakestoreapi.com/products',{server:false})

</script>

<style lang="scss" scoped>

</style>