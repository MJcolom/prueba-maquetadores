<template>
    <div>
        <div class=" relative text-white">
            <img class="shadow-xl  w-full hover:shadow-2xl" src="../assets/img/portada.webp">
            <div class=" absolute top-8  grid grid-cols-4 sm:grid-cols-6 xl:grid-cols-12 gap-1 w-full ">
                <div class=" col-start-1 xl:col-start-2 col-span-4  sm:col-span-2 xl:col-span-5 font-bold">Refineria Web</div>
                <div class=" text-center" v-for="(element, index) in menu" :key="index">{{ element.nombre }}</div>
            </div>
            <div class=" absolute top-2/4  flex flex-col items-center justify-center w-full">
                <div class="text-3xl mt-4 sm:mt-0 sm:text-5xl">Construimos tus sueños</div>
                <div class="mx-32 text-center mt-6" v-if="window.width > 765">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime mollitia,
                    molestiae quas vel sint commodi repudiandae consequuntur voluptatum laborum
                    numquam blanditiis harum quisquam eius sed odit fugiat iusto fuga praesentium
                    optio, eaque rerum!
                </div>
                <div v-if="window.width > 1024"> 
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-auto w-20 mt-20 cursor-pointer" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
                    </svg>
                </div>
                
            </div>
        </div>
        <div class=" my-14 gap-20 grid grid-cols-1 sm:grid-cols-3 xl:grid-cols-5  mx-2">
            <div class=" col-start-1 xl:col-start-2  grid grid-rows-1" >
                <span class="text-4xl leading-relaxed border-b-4 mb-5">Lorem ipsum</span>
                <span>Provident similique accusantium nemo autem. Veritatis
                    obcaecati tenetur iure eius earum ut molestias architecto voluptate aliquam
                    nihil, eveniet aliquid culpa officia aut!
                </span>
                
            </div>
            <div class="grid grid-rows-1"  v-for="n in 2" :key="n">
                <span class="text-4xl leading-relaxed border-b-4 mb-5">Lorem ipsum</span>
                <span>Provident similique accusantium nemo autem. Veritatis
                    obcaecati tenetur iure eius earum ut molestias architecto voluptate aliquam
                    nihil, eveniet aliquid culpa officia aut!
                </span>
                
            </div>
        </div>
        <div class=" relative text-black text-sm xl:text-2xl bg-purple-100">
            <img class="w-3/5" src="../assets/img/plazos.jpg">
            
            <div class="absolute top-1 sm:top-1/4 grid grid-cols-2 gap-3 xl:grid-cols-4 ">
                <div class=" col-start-2 xl:col-start-3 col-span-1 xl:col-span-2 grid-rows-1">
                    <div class="text-3xl font-bold">Cumplimos los plazos</div>
                    <div class=" mr-0 xl:mr-64 text-xs sm:text-sm" v-if="window.width > 765">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                        Donec gravida tincidunt euismod. Mauris lacus mi, vulputate eget sem
                        vitae, imperdiet consectetur urna.
                    </div>
                    <button class="bg-blue-500 hover:bg-blue-700 w-1/2  mt-4 text-white font-bold py-2 px-4 rounded">
                        Contacto
                    </button>
                </div>
               
            </div>
        </div>
        <div class=" my-14 gap-4 grid grid-cols-1 sm:grid-cols-4 xl:grid-cols-6">
            <div class=" col-start-1 xl:col-start-2 grid grid-rows-1">
                <svg class="h-20 w-10 text-blue-500 mx-auto"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round">  <polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2" /></svg>
                <span class="text-4xl leading-relaxed text-center">Lorem ipsum</span>
                <span class="text-center">Provident similique accusantium nemo autem. Veritatis
                    obcaecati tenetur iure eius earum ut molestias architecto voluptate aliquam
                    nihil, eveniet aliquid culpa officia aut!
                </span>
                
            </div>
            <div class="grid grid-rows-1"   v-for="n in 3" :key="n">
                <svg class="h-20 w-10 text-blue-500 mx-auto"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round">  <polygon points="13 2 3 14 12 14 11 22 21 10 12 10 13 2" /></svg>
                <span class="text-4xl leading-relaxed text-center">Lorem ipsum</span>
                <span class="text-center">Provident similique accusantium nemo autem. Veritatis
                    obcaecati tenetur iure eius earum ut molestias architecto voluptate aliquam
                    nihil, eveniet aliquid culpa officia aut!
                </span>
                
            </div>
        </div>
        <div class="bg-gray-800 mt-20 xl:mt-40  h-96">
            <div class="grid grid-cols-1 xl:grid-cols-3 h-full content-center">
                <div class="col-start-1 xl:col-start-2  grid grid-rows-1  gap-4  mx-16 xl:mx-0">
                    <div class="text-center text-white text-3xl"> "Integer ut ex vitae enim semper"</div>
                    <div class="text-gray-400 text-center">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit.
                        Donec gravida tincidunt euismod.
                    </div>
                    <button class="bg-blue-500 hover:bg-blue-700 w-2/4 mx-auto text-white font-bold py-2 px-4 rounded">
                        Button
                    </button>
                </div>
            </div>
        </div>
    </div>
    
</template>

<script>
    export default {
        props: ['menu'],
        data() {
            return {
                window: {
                    width: 0,
                    height: 0
            }
        }
     },
    created() {
        window.addEventListener('resize', this.handleResize);
        this.handleResize();
    },
    destroyed() {
        window.removeEventListener('resize', this.handleResize);
    },
    methods: {
        handleResize() {
            this.window.width = window.innerWidth;
            this.window.height = window.innerHeight;
        }
    }
    }
</script>

<style scoped>
</style>