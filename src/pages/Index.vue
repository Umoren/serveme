<template>
  <Layout class="">
    
    <div class=" my-8 container mx-auto px-4 py-4">
      <section class="md:flex my-4 flex-wrap">
        <div class="md:w-1/2  md:block">
          <h2 class="text-yellow-500 text-xl font-semibold leading-normal "> Basic Services </h2>
          <h1 class="text-4xl font-bold leading-normal "> We do all your <span class="text-pri">basic chores </span> and let you to be productive</h1>
          <p class="my-4 font-light "> Get your stuff done in very short time with just $3/hr. Reliable and fast service.</p>

          <div>
            <g-image class="call-us" src="../assets/images/phone-call.svg" alt="Customer care" />
            <p class="text-xl  font-semibold"> Call for appointment: <a class="text-pri" href="tel:+08171942286">08171942286</a> </p>
          </div>
        </div>

        <div class="hidden md:hidden lg:block md:w-1/2 max-h-screen ">
          
            <svg class="align__svg" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg">
              <path fill="#24A148" d="M40.7,-54.5C55,-45.7,70.4,-36.8,78.3,-22.9C86.3,-9.1,87,9.7,81.9,27C76.8,44.2,65.9,60,51.3,61.5C36.7,63.1,18.4,50.4,1.1,48.8C-16.1,47.2,-32.1,56.8,-46.4,55.1C-60.6,53.5,-73,40.6,-77.1,25.6C-81.2,10.6,-76.9,-6.5,-71.6,-23.3C-66.2,-40.2,-59.7,-56.7,-47.6,-66.2C-35.5,-75.7,-17.7,-78.2,-2.3,-75.1C13.2,-71.9,26.5,-63.3,40.7,-54.5Z" transform="translate(100 100)" />
            </svg>

            <g-image  class="image__edit" src="../assets/images/cleaner1.png" alt="lady cleaning" />
        
        </div>
      </section>

  
      <section class="mb-16">
        <div class="text-center">
            <h1 class="text-4xl font-bold leading-normal "> How it works</h1>
        </div>

        <div class="flex justify-center my-8">
          <div>
            <button class="bg-transparent hover:bg-green-500 text-green-700 font-semibold hover:text-white h-16 w-16  py-2 px-4 border border-green-500 hover:border-transparent rounded-full">
              1
            </button>

          </div>
          <hr />
          <div>
           <button class="bg-transparent hover:bg-green-500 text-green-700 font-semibold hover:text-white h-16 w-16  py-2 px-4 border border-green-500 hover:border-transparent rounded-full">
              2
            </button>
          </div>
          <hr />
          <div>
           <button class="bg-transparent hover:bg-green-500 text-green-700 font-semibold hover:text-white h-16 w-16  py-2 px-4 border border-green-500 hover:border-transparent rounded-full">
              3
            </button>
          </div>
        </div> 

        <div class="md:flex lg:flex  justify-center mx-4  md:text-center">
          <div class="md:w-1/3 my-2 lg:w-1/3 mx-4 sm:w-auto overflow-hidden shadow-sm bg-yellow-100 bg-opacity-25 rounded-lg py-3 px-2">
              <g-image class="object-cover w-8 md:m-auto h-8 " src="~/assets/images/tap.svg" />
              <h2 class="text-bold text-xl"> Choose your Server </h2>
              <p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Neque, provident. </p>
          </div>

          <div class="md:w-1/3 my-2 lg:w-1/3 mx-4 sm:w-auto overflow-hidden shadow-sm bg-yellow-100 bg-opacity-25 rounded-lg py-3  px-3">
              <g-image class="object-cover w-8 m-auto h-8" src="~/assets/images/payment.svg" />
              <h2 class="text-bold text-xl" > Pay and confirm </h2>
              <p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Neque, provident. </p>
          </div>

          <div class="md:w-1/3 my-2 lg:w-1/3 mx-4 sm:w-auto overflow-hidden shadow-sm bg-yellow-100 bg-opacity-25 rounded-lg py-3  px-3">
              <g-image class="object-cover w-8 m-auto h-8" src="~/assets/images/review.svg" />
              <h2 class="text-bold text-xl"> Send a review </h2>
              <p> Lorem ipsum dolor sit amet consectetur adipisicing elit. Neque, provident. </p>
          </div>
        </div>
      </section>

      
      <section class="mt-32">
        <div class="md:w-2/3 sm:w-auto ">
            <h1 class="text-4xl font-bold leading-normal "> Here are the things we can do for you</h1>
        </div>

        <div class="md:flex flex-wrap my-4 -mx-4">
          <div class="w-full px-4 lg:w-1/3  md:w-1/3 my-3" v-for="service in allServices" :key="service.id">
             <ServiceCard :service="service" />
          </div>
         
        </div>
      </section>

      <!-- Contact -->

      <section class="mt-32"> 
       
        <ContactForm />
      </section>

      
    </div>

   


  </Layout>
</template>

<script>
import ServiceCard from '~/components/ServiceCard.vue';
import ContactForm from '~/components/ContactForm.vue';

export default {
  metaInfo: {
    title: 'Serve Me'
  },
  components: {
    ServiceCard,
    ContactForm,
   
  },
  data () {
    return {
      allServices: [ 
      {
        title: "Apartment Cleaning",
        imgUrl: "https://res.cloudinary.com/samtech/image/upload/v1596679720/cleaning.svg",
        imgAlt: "Cleaning",
        description: " Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil."
      },
       {
        title: "Office Cleaning",
        imgUrl: "https://res.cloudinary.com/samtech/image/upload/v1596679720/furniture.svg",
        imgAlt: "Office Cleaning",
        description: " Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil."
      },
      {
        title: "Home Tutor",
        imgUrl: "https://res.cloudinary.com/samtech/image/upload/v1596679722/tutor.svg",
        imgAlt: "Home Tutor",
        description: " Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil."
      },
      {
        title: "Virtual Assistance",
        imgUrl: "https://res.cloudinary.com/samtech/image/upload/v1596679720/robot.svg",
        imgAlt: "Robot",
        description: " Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil."
      },
      {
        title: "Domestic Chores",
        imgUrl: "https://res.cloudinary.com/samtech/image/upload/v1596679720/household-chores.svg",
        imgAlt: "Domestic Chores",
        description: " Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil."
      },
      {
        title: "More",
        imgUrl: "https://res.cloudinary.com/samtech/image/upload/v1596679720/more.svg",
        imgAlt: "More",
        description: " Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil."
      },
    ]
  }
}
}
</script>

<style >

 a:link{
   color: #0E5849;
 }
 
  span.text-pri{
     color: #0E5849;
  }

  .bg-primary{
     background-color: #0E5849;
  }
  hr{
    flex-basis: 30%;
    margin-top: 2em;
    margin-bottom: 2em;
    border-width: .1em;
    background-color: #0E5849;
  }

  .call-us{
    width: 20em;
  }

  .align__svg{
    position: relative;
    left: 3em;
    top: -5em;
    right: 0;
    bottom: 0;
  }

@media (min-width: 910px){
  .image__edit{
    
    width: 47%;
    /* border: none; */
    background: #F9F7F1;
    position: relative;
    top: -39em;
    left: 13em;
    z-index: 1;
    border-bottom-left-radius: 7em;
    border-top-left-radius: 4em;
    border-top-right-radius: 4em;
    transform: rotate(deg);
    border-bottom-right-radius: 9em;
  }

 
}
</style>
