<template>
     <form class="w-full py-8 px-4 md:px-12 bg-green-100 rounded-lg bg-opacity-50">
        <h2 class="font-extrabold text-2xl"> Join our waiting list </h2>
        
        <div class="md:flex my-6">
            <div class="md:w-1/2 ">
                <div class="my-4">
                    <input class="appearance-none border rounded md:w-3/4 w-full py-4 px-3 bg-white bg-opacity-50 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="Name">
                </div>

                <div class="my-4">
                    <input class="appearance-none border rounded md:w-3/4 w-full py-4 px-3 bg-white bg-opacity-50 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="email" type="email" placeholder="myemail@email.com">
                </div>

                <div class="my-4">
                    <div class="inline-block relative">
                        <select class="block appearance-none md:2/2 w-full   bg-white bg-opacity-50 border border-gray-400 hover:border-gray-500 py-4 px-3 pr-8 rounded  leading-tight focus:outline-none focus:shadow-outline">
                            <option value="" selected disabled> Select a Service</option>
                            <option value="" v-for="listItem in listOptions" :key="listItem.id" > {{listItem}}</option>
                        </select>
                        <div class="pointer-events-none absolute inset-y-0 right-0 flex items-center px-2 text-gray-700">
                            <svg class="fill-current h-4 w-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z"/></svg>
                        </div>
                    </div>
                </div>

                <div class="my-4">
                    <textarea name="" class="appearance-none border rounded lg:1/2 md:w-3/4 w-full py-4 px-3 bg-white bg-opacity-50 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"  placeholder="Message"></textarea>
                </div>

                <div class="md:w-1/2">
                    <button type="submit" class="w-full  bg-primary hover:bg-primary  text-white shadow-inner bg-opacity-50 font-bold py-2 px-6 rounded"> Send </button>
                </div>
            </div>

            <div class="hidden md:block md:w-1/2">
                <div class="md:w-auto "> 
                    <g-image class="m-auto shadow-lg object-cover b-rad1" src="~/assets/images/clean.jpg" alt="Cleaning" />
                </div>
            </div>


        </div>
    </form>
</template>

<script>
export default {
    name: 'ContactForm',

    data() {
        return{
            listOptions: ['Apartment Cleaning', 'Office Cleaning', 'Home Tutor', 'Virtual Assistance', 'Domestic Chores']
        }
    }
}
</script>

<style scoped>
    .b-rad1{
        border-bottom-right-radius: 35%;
        border-top-left-radius: 35%;
        border-color: #0E5849;
        border-width: .4em;
        max-width: 50%;
        height: auto;
    }

</style>