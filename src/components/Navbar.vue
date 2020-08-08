<template>
  <header class=" sm:flex sm:justify-between sm:items-center sm:px-4 sm:py-3">
    <div class="flex items-center justify-between px-4 py-3 sm:p-0">
      <div>
        <h3 class="font-bold text-2xl text-black"> <span id="override-color">S</span>erve Me </h3>
      </div>
      <div class="sm:hidden">
        <button @click="isOpen = !isOpen" type="button" class="block text-gray-500 hover:text-dark focus:text-dark focus:outline-none">
          <svg class="h-6 w-6 fill-current" viewBox="0 0 24 24">
            <path v-if="isOpen" fill-rule="evenodd" d="M18.278 16.864a1 1 0 0 1-1.414 1.414l-4.829-4.828-4.828 4.828a1 1 0 0 1-1.414-1.414l4.828-4.829-4.828-4.828a1 1 0 0 1 1.414-1.414l4.829 4.828 4.828-4.828a1 1 0 1 1 1.414 1.414l-4.828 4.829 4.828 4.828z"/>
            <path v-if="!isOpen" fill-rule="evenodd" d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"/>
          </svg>
        </button>
      </div>
    </div>
    <nav :class="isOpen ? 'block' : 'hidden'" class="px-2 pt-2 pb-4 align-center sm:flex sm:p-0 w-1/2 justify-around">
     <div class="sm:flex align-center">
        <a href="#" class="block px-2 py-1 navitem__color font-semibold rounded  ">List your property</a>
        <a href="#" class="mt-1 block px-2 py-1 navitem__color font-semibold rounded   sm:mt-0 sm:ml-2">Trips</a>
        <a href="#" class="mt-1 block px-2 py-1 navitem__color font-semibold rounded   sm:mt-0 sm:ml-2">Messages</a>
     </div>

     <div class="flex">
         <button class="btn btn-call "> Call us now </button>
     </div>
    </nav>
  </header>
</template>
    

<script>
    export default {
        data() {
            return{
                isOpen: false
            }
        }
    }
</script>

<style>
    .navitem__color{
        color: #0E5849;
    }
    .navitem__color:hover{
         color: #0E5849;
        /* background: #0E5849; */
    }
    .bg-primary{
        background: #0E5849;
    }
    
    .btn{
        @apply font-bold py-2 px-4 rounded;
    }

    .btn-call{
        @apply text-white bg-primary;
        border-top-left-radius: 5em;
        border-bottom-left-radius: 5em;
        border-bottom-right-radius: 5em;
    }
    
</style>
