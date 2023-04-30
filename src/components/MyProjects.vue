<template>
    <section class="pt-60 text-center">
        <p class="" id="projects">Latest</p>
        <h1 class="text-9xl font-semibold uppercase py-8">
            Projects
        </h1>
        <p class="text-2xl pb-12">Oppurtunities that challenged to learn</p>
    </section>
    <section class="grid md:grid-cols-2 gap-4 w-11/12 mx-auto text-gray-100">
        <div class="bg-gray-900 rounded p-4" v-for="(project, index) in projects" :key="index">

            <p class="">{{ project.location }}</p>
            <h2 class="text-5xl font-bold text-center py-8">{{ project.pName }}</h2>
            <div class="grid grid-cols-3 w-10/12 mx-auto gap-3 pl-8 py-4 h-32">
                <div class="flex gap-2" v-for="(skill, index) in project.skills" :key="index">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                        stroke="currentColor" class="w-6 h-6">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M4.5 12.75l6 6 9-13.5" />
                    </svg>

                    <p>{{ skill }}</p>
                </div>
            </div>
            <p class="w-11/12 mx-auto text-justify line-clamp-4">{{ project.pDescription }}</p>
            <div class="flex justify-between pt-6">
                <div class="">
                    <p v-if="project.cWorking"
                        class="rounded-full bg-gray-50 text-gray-900 font-bold py-1 uppercase px-2 text-sm">
                        In Progress</p>
                </div>
                <p class="font-light italic">{{ project.duration[0] }} - {{ project.duration[1] }}</p>
            </div>
        </div>
    </section>
    <!-- {{ projects }} -->
</template>
<script>
export default {
    name: "MyProjects",
    props: {
        projects: Array
    }
}
</script>
<style lang="">
    
</style>