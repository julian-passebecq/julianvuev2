<template>
  <nav
    id="navbar"
    class="bg-white border-gray-200 px-2 sm:px-4 dark:bg-gray-900"
  >
    <div
      class="container flex flex-wrap justify-between items-center mx-auto flex items-center"
    >
      <span
        id="nav-title"
        class="leading-none self-center text-2xl sm:text-4xl font-semibold whitespace-nowrap text-white md:text-5xl mt-1 mb-2"
        ><u>Julian PASSEBECQ</u><br>  Energy Engineer<br>4 years Data Exp</span>
       
      
      

        <div class="graph_one">
        <table
        id="animations-example-6"
        class="charts-css column show-labels hide-data data-spacing-5 show-primary-axis"
      >
        <tbody>
          <tr>
            <th scope="row">BI</th>
            <td class="td_one"></td>
          </tr>
          <tr>
            <th scope="row">SQL</th>
            <td class="td_two"></td>
          </tr>
          <tr>
            <th scope="row">ETL</th>
            <td class="td_three"></td>
          </tr>
          <tr>
            <th scope="row">DATA</th>
            <td class="td_four"></td>
          </tr>
          <tr>
            <th scope="row">CLOUD</th>
            <td class="td_five"></td>
          </tr>
         
        </tbody> 
      </table> 
      </div>
      <div class="w-auto text-white py-2.5" id="navbar-buttons">
        <button
          @click="showReadme"
          class="nav-button text-sm sm:text-lg bg-white hover:bg-black hover:text-white text-black font-bold py-1 px-2 md:px-4 rounded inline-flex items-center mr-2.5"
        >
        <svg  xmlns="http://www.w3.org/2000/svg" class="mr-1 nav-icon w-4 h-4 lg:w-6 lg:h-6"
        viewBox="0 0 24 24"> >
        
        <path d="M3 24h19v-23h-1v22h-18v1zm17-24h-18v22h18v-22zm-3 17h-12v1h12v-1zm0-3h-12v1h12v-1zm0-3h-12v1h12v-1zm-7.348-3.863l.948.3c-.145.529-.387.922-.725 1.178-.338.257-.767.385-1.287.385-.643 0-1.171-.22-1.585-.659-.414-.439-.621-1.04-.621-1.802 0-.806.208-1.432.624-1.878.416-.446.963-.669 1.642-.669.592 0 1.073.175 1.443.525.221.207.386.505.496.892l-.968.231c-.057-.251-.177-.449-.358-.594-.182-.146-.403-.218-.663-.218-.359 0-.65.129-.874.386-.223.258-.335.675-.335 1.252 0 .613.11 1.049.331 1.308.22.26.506.39.858.39.26 0 .484-.082.671-.248.187-.165.322-.425.403-.779zm3.023 1.78l-1.731-4.842h1.06l1.226 3.584 1.186-3.584h1.037l-1.734 4.842h-1.044z"/>
      </svg>
          
          <span class="mt-1">CV</span>
        </button>
      </div>
        
        
      </div>
    
    
  </nav>
</template>

<style>

.graph_one {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0px 10px;
  
}

graph_one {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}


#animations-example-6 td {
  background-image: linear-gradient(
    90deg,
    #000000,
    #000000,
    #000001,
    #000000,
    #0000009b,
    #020500
  );


  background-size: 600%;
  animation: gradient-animation 3s linear infinite alternate;
}
@keyframes gradient-animation {
  0% {
    background-position: 0%;
  }
  100% {
    background-position: 100%;
  }

}
.graph_one {
  margin-top: 0px;
  margin-bottom: -5px;
  margin-left:-20px;
  margin-right:-15px;
}
.graph_one th {
  color: #000000;
  margin-top: 0px;
  font-style: italic;
  font-weight: 200;
  font-size: 6px;
}
.graph_one tr {
  display: flex !important;
  flex-direction: column-reverse !important;
  width: 15px;
  margin: 5px;
}
.graph_one td {
  border: 1px solid #fff;
}
.graph_one .td_one {
  height: 35px;
}
.graph_one .td_two {
  height: 20px;
}
.graph_one .td_three {
  height: 15px;
}
.graph_one .td_four {
  height: 30px;
}
.graph_one .td_five {
  height: 15px;
}
.graph_one tbody {
  display: flex !important;
}

@font-face {
  font-display: swap;
  
}



#nav-title {
  text-shadow: 1px 1px 0 #000, -1px -1px 0 #000, 1px -1px 0 #000,
    -1px 1px 0 #000, 1px 1px 0 #000;
  font-family: "Anvir", serif;
  font-size: 13px;
 margin-left: 5px;
  text-align:left;
  
}
#navbar {
  background-color: #a7ccff;
  
}
.nav-button:hover .nav-icon {
  fill: #ffffff;
}
</style>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  methods: {
    showReadme() {
      this.$emit("showReadme", true);
    },
  },
});
</script>
