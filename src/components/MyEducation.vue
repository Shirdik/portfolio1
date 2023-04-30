<template>
    <div class="py-8" id="education">
        <h2 class=" text-lg py-4">Education</h2>
        <div class="flex justify-between items-end">
            <h1 class="text-5xl font-semibold">
                Where it all<br>started
            </h1>
        </div>
        <div class="flex flex-col items-center justify-center gap-3 py-4 ">
            <div class="w-full rounded border-dotted border-gray-300 pb-4 border-b-4" v-for="(item, index) in education"
                :key="index">
                <div class="flex justify-between items-center">
                    <div class="">
                        <p class="py-2">{{ item.eName }}
                            <span v-if="item.pursuing"
                                class="uppercase bg-gray-300 text-gray-700 px-4 py-1 rounded-full font-bold text-xs mx-2">in
                                progress</span>
                        </p>
                        <p class="font-semibold text-xl pb-2">
                            {{ item.concentration }}</p>
                        <p class="p-2 border-2 rounded-full border-gray-300 max-w-fit w-12 h-12">
                            {{ item.grade[0] }}/{{ item.grade[1] }}
                        </p>

                    </div>
                    <div class=" text-right">
                        <p class="py-2">{{ item.institution }}
                        </p>
                        <span class="text-gray-600 text-sm italic pb-2">{{ item.Location }}</span>
                        <p class="italic text-lg"> <span class="font-semibold pr-2 text-md ">passout:</span>{{ item.passout
                        }}</p>
                    </div>
                </div>
            </div>
        </div>
        <!-- {{ education }} -->
    </div>
</template>
<script>
export default {
    name: 'MyEducation',
    props: {
        education: Array
    }
}
</script>
<style lang="">
    
</style>