<template #fallback>
    <article class="rounded-xl  truncate bg-white p-3 shadow-lg hover:shadow-xl hover:transform hover:scale-105 duration-300 ">
      <a href="#">
        <div class="relative flex items-center justify-center overflow-hidden rounded-xl">
          <img :src="image" class="w-48 h-60"     alt="Hotel Photo" />
          
        </div>

        <div class="mt-1 p-2 ">
          <h2 class="text-slate-700">{{ title }}</h2>
          <p class="mt-1 h-20 text-sm text-slate-400 text-ellipsis  overflow-hidden  ">{{ description }}</p>

          <div class="mt-3 flex items-end justify-between">
              <p class="text-lg font-bold text-blue-500">{{ price*1000 }} FT</p>

            
          </div>
        </div>
      </a>
    </article>
</template>

<script setup>
const {title,price,image,id,description,category} =  defineProps(["title", "price", "image", "id", "description","category"])
</script>

<style lang="scss" scoped>

</style>