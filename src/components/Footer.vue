<template>
    <div class="container mx-auto px-4 ">
        <ul class="flex flex-wrap w-2/3 justify-between">
            <h3 class="font-bold text-2xl text-black"> <span id="override-color">S</span>erve Me </h3>
            <li><a class="mt-1 block px-2 py-1 navitem__color text-sm font-semibold rounded text-xl  sm:mt-0 sm:ml-2"> Home </a></li>
            <li><a class="mt-1 block px-2 py-1 navitem__color text-sm font-semibold rounded text-xl  sm:mt-0 sm:ml-2"> Services </a></li>
            <li><a class="mt-1 block px-2 py-1 navitem__color text-sm font-semibold rounded text-xl  sm:mt-0 sm:ml-2"> About </a></li>
            <li><a class="mt-1 block px-2 py-1 navitem__color text-sm font-semibold rounded text-xl  sm:mt-0 sm:ml-2"> Contact us </a></li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'Footer'
}
</script>

<style scoped>
    ul{
        list-style: none;
    }
</style>