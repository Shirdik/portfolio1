<template>
    <p class="uppercase text-center text-8xl font-extrabold py-4 tracking-wider ">
        {{ personal.fullName }}
    </p>
    <div class="grid grid-cols-4 text-center gap-6 py-4">
        <div class="" v-for="(value, key) in  social " :key="key">
            <a v-bind:href="value" class="underline">{{ key }}</a>
        </div>
    </div>
</template>
<script>
export default {
    name: 'MyHeader',
    props: {
        personal: Object,
        social: Object
    }
}
</script>
<style></style>