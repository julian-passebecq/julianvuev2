<template>
  <vue-final-modal
    v-slot="{ params, close }"
    v-bind="$attrs"
    v-model="showModalModel"
    classes="flex justify-center items-center"
    content-class="relative flex flex-col max-h-full mx-4 p-4 border rounded bg-night-blue text-white"
    @closed="closed"
    :transition="{
      'enter-active-class': 'transition duration-350 ease-in-out transform',
      'enter-class': 'translate-y-full',
      'enter-to-class': 'translate-y-0',
      'leave-active-class': 'transition duration-350 ease-in-out transform',
      'leave-to-class': 'translate-y-full',
      'leave-class': 'translate-y-0',
    }"
  >
    <div
      class="flex-grow overflow-y-auto text-left sm: px-6 xl:px-32 max-w-lg lg:max-w-2xl xl:max-w-3xl 2xl:max-w-7xl"
    >
      <slot v-bind:params="params"></slot>
      <h1 v-if="isPrerender" class="text-3xl">
      </h1>
      </div>
      <h2 class="text-2xl mt-8 font-bold text-white">CONTACT & CV</h2>
      <div class="ml-2 md:ml-4">
        <h3>

          Resume :
            <a href="https://www.canva.com/design/DAFUwYINHnc/qa3FKY9sIE22C8ffUx18qA/view?utm_content=DAFUwYINHnc&utm_campaign=designshare&utm_medium=link&utm_source=publishsharelink" 
            target="_blank"><u> PDF</u></a>
         </h3>

         <h3><br>
          Phone :
          
          <a href="tel:+33 7 67 42 48 98"  target="_blank" ><u>+33 7 67 42 48 98</u></a> 
          
        </h3>

        <h3><br>
          Linkedin:
          
          <a href="https://www.linkedin.com/julian-p95"  target="_blank" ><u>Julian Passebecq</u></a> 
          
        </h3>

         <h3>
           Professional Github :
           
           <a href="https://github.com/julian-p95" target="_blank"><u>Julian-p95</u></a> 
         </h3><h3>
          Email :
          
          <a href="mailto:julian.passebecq@gmail.com"><u>julian.passebecq@gmail.com</u></a> 
        </h3>
        
        

        
       
      </div>
      <h2 class="text-2xl mt-8 font-bold text-white">WORK EXP </h2>
      <div class="ml-2 md:ml-4">
        
       
      </div>

        
        <h2 class="text-xl mt-6">2022: Danone,Digital Manager</h2>
        

       <h2 class="text-xl mt-6">2020/21: Startup,Data Sc</h2>
      
        

        <h2 class="text-xl mt-6">2020: Consulting Data PMO</h2>
      
        
        <h2 class="text-xl mt-6">2018/19: TOTAL,Product Own</h2>
      
        
      <h2 class="text-xl mt-6">2017: SAVENCIA, Data Intern</h2>
     
      

      
      
   
    <button
      @click="closed"
      class="absolute top-0 right-2 mt-2 mr-2 text-2xl sm:text-base"
    >
      X
    </button>
  </vue-final-modal>
</template>

<script>
import { VueFinalModal, ModalsContainer } from "vue-final-modal";

export default {
  props: {
    showModal: {
      type: Boolean,
      required: true,
    },
    isPrerender: {
      type: Boolean,
      required: true,
    },
  },
  computed: {
    showModalModel: {
      get () {
        return this.showModal
      },
      set (value) {
        if (value === false) {
          this.closed()
        }
      }
    },
  },
  name: "Readme",
  components: {
    VueFinalModal,
    ModalsContainer,
  },
  methods: {
    closed() {
      this.$emit("close");
    },
  },
};
</script>
