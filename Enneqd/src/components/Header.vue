<script setup>
    import { reactive } from 'vue';

    const state = reactive({hidesearch:true});
</script>

<template>
    <header class="w-full bg-orange-400 p-0">
        <div class="flex flex-row justify-between items-center">
            <div class="my-2 pl-5">
                <h1 class="text-xl font-medium md:text-3xl">Enne9d</h1>
            </div>

            <div class="flex items-center h-full">
                <div class="h-full flex">
                    <input v-if="!state.hidesearch" class="w-full md:block bg-slate-50 outline-none px-1 border rounded-md" type="search" placeholder="search...">
                    <button class="md:hidden" @click="state.hidesearch = !state.hidesearch">S</button>
                    
                </div>

                <div class="px-2 h-full">
                    <p class="float-right">Sign In</p>
                </div>
            </div>
            
        </div>
        <div class="w-full sm:"> 
            <ul class="flex flex-row items-center justify-center gap-3 text-nowrap mb-10">
                <li>Hot!</li>
                <li>Top Rated</li>
                <li>Trending Reviews</li>
            </ul>
        </div>
    </header>

</template>

<style scoped>
</style>