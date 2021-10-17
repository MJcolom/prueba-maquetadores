<template>
    <div class=" bg-gray-900 text-white ">
        <div class=" grid grid-rows-1 grid-cols-3 sm:grid-cols-10  text-xs gap-3">
            <div class="col-start-1 sm:col-start-2 sm:col-span-3  my-2">Lorem ipsum dolor sit amet</div> 
            <div class=" col-start-2 sm:col-start-7 col-span-1 sm:col-span-2 my-2">
                <span class="icon">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 22 22" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                    </svg>
                </span>
               <span  class="icon">+34 777 886 555</span> 
            </div>
            <div class=" col-start-3 sm:col-start-9  my-2 col-span-1 sm:col-span-2">
                <span class="icon"><img src="https://img.icons8.com/material-outlined/24/FFFFFF/whatsapp--v1.png"/></span>
                
                <span class="icon">+34 777 886 555</span> 
            </div>
        </div>
        
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.icon,
.text {
  vertical-align: middle;
  display: inline-block;
}
</style>