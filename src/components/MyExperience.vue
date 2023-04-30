<template>
    <div class="" id="experience">
        <h2 class=" text-lg py-4">Experience</h2>
        <div class="flex justify-between items-end">
            <h1 class="text-5xl font-semibold">
                Platforms that gave<br>a chance to grow.
            </h1>
        </div>
        <div class="grid grid-cols-3 py-8 gap-4 w-11/12 mx-auto">
            <div class="bg-white rounded" v-for="(xp, i) in experience" :key="i">
                <div class="h-56 bg-gray-400 rounded"></div>
                <div class="py-2 px-3 border-b border-slate-300">
                    <p class="">{{ xp.employer }}</p>
                    <p class="font-semibold py-1 text-2xl">{{ xp.role }}</p>
                    <p class="text-justify line-clamp-5"> {{ xp.description }}</p>
                    <p class="text-right italic text-black/70 font-light pt-2 pb-1">{{ xp.duration[0] }} - {{ xp.duration[1]
                    }}
                    </p>
                </div>
                <div class="flex justify-between px-3 py-2 bg-gray-200 rounded-b">
                    <p>More...</p>
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                        stroke="currentColor" class="w-6 h-6">
                        <path stroke-linecap="round" stroke-linejoin="round"
                            d="M4.5 12h15m0 0l-6.75-6.75M19.5 12l-6.75 6.75" />
                    </svg>

                </div>
            </div>
        </div>
        <!-- {{ experience }} -->
    </div>
</template>
<script>
export default {
    name: 'MyExperience',
    props: {
        experience: Array
    }
}
</script>
<style lang="">
    
</style>