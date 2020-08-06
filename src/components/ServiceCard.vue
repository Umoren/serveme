<template>
    <div class=" overflow-hidden shadow-sm bg-yellow-100 bg-opacity-25 rounded-lg pt-4">
        <div class="w-16 h-16 grid content-center m-auto">
            <g-image class="w-full object-cover" :src="service.imgUrl" :alt="service.imgAlt" />
        </div>
        <div class="px-6 py-4 text-center">
            <div class="font-bold text-xl mb-2">
                <h2>{{service.title}}</h2>
            </div>
            <p class="text-gray-700 text-base">
                {{service.description}}
            </p>
        </div>
    </div>
</template>

<script>
export default {
    props: ['service']
}
</script>