<template>
    <div class="py-4">
        <nav class="flex justify-between items-center py-4">
            <div class="flex gap-12 items-center">
                <p class="pr-4 font-semibold text-2xl ">SK</p>
            </div>
            <div class="flex items-center gap-4">
                <a href="">Home</a>
                <a href="#skills">Skills</a>
                <a href="#experience">Experience</a>
                <a href="#projects">Projects</a>
            </div>
            <div class="">
                <a v-bind:href="email" class="">Contact Me</a>
            </div>
        </nav>
    </div>
</template>
<script>
export default {
    name: 'NavBar',
    props: {
        email: String
    }


}
</script>
<style lang="">
    
</style>