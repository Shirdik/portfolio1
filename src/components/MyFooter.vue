<template>
    <!-- {{ education }} -->
    <h1 class="font-semibold text-2xl py-8">SK</h1>
    <div class="font-semibold border-dotted border-gray-300 pb-4 border-b-4">
        <div class="flex items-center gap-4">
            <a href="">Home</a>
            <a href="#skills">Skills</a>
            <a href="#experience">Experience</a>
            <a href="#projects">Projects</a>
        </div>
    </div>
    <div class="flex justify-end gap-6 py-4">
        <p class="font-semibold">Connect:</p>
        <div class="" v-for="(value, key) in social" :key="key">
            <a v-bind:href="value">{{ key }}</a>
        </div>
    </div>
    <!-- {{ social }} -->
</template>
<script>
export default {
    name: 'MyFooter',
    props: {
        social: Object
    }
}
</script>
<style lang="">
    
</style>