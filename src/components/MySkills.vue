<template>
    <div class="py-8" id="skills">
        <h2 class=" text-lg py-4">Skills</h2>
        <div class="flex justify-between items-end">
            <h1 class="text-5xl font-semibold">
                Tools needed to<br>get work done.
            </h1>
            <p class=""> These get updated <span class="font-semibold">regularly.</span></p>
        </div>
        <div class="grid grid-cols-5 py-8 gap-4 w-11/12 mx-auto">
            <div class="flex justify-start items-center gap-3" v-for="(skill, i) in skills" :key="i">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                    stroke="currentColor" class="w-6 h-6">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M17.25 8.25L21 12m0 0l-3.75 3.75M21 12H3" />
                </svg>
                <p>{{ skill }}</p>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'MySkills',
    props: {
        skills: Array
    }
}
</script>
<style lang="">
    
</style>