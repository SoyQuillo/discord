<script setup>

import { ref } from 'vue';

let index = ref(0);

let mensajes =[{
  name:'Marco Perez',
  mensaje1: 'Hola como estas',
  mensaje2: 'fulbito?',
  mensaje3: 'toca ir a la u?'
},
{
  name:'Juanito Alimaña',
  mensaje1: 'que haces xd',
  mensaje2: 'un lolsito?',
  mensaje3: 'juguemos valorant'
}]

function doClickMaestroSplinter(indice){
index.value = indice
}


</script>

<template>

<div class="flex container max-w-4xl bg-gray-700 mt-12 justify-between mx-auto rounded-md">
  <div class="rounded-md bg-slate-800 p-2">
    <div class="bg-[url('https://steamuserimages-a.akamaihd.net/ugc/2059873190232684844/BE10D8DBA2FCE3530A7C20507FCE034F1AD7605B/?imw=512&&ima=fit&impolicy=Letterbox&imcolor=%23000000&letterbox=false')] bg-cover w-10 mx-auto h-10 rounded-md mt-5">
    </div>
    <div class="text-center text-gray-300">Perfil</div>
  </div>


  <div class="p-2">
   <div><h1 class="text-gray-300 text-xl text-center mb-4">Tendencias</h1></div>
   <div class="bg-gray-600 mt-2 rounded-lg"><p  class="text-gray-300 text-center">#Messi</p></div>
   <div class="bg-gray-600 mt-2 rounded-lg"><p class="text-gray-300 text-center">#Messi</p></div>
   <div class="bg-gray-600 mt-2 rounded-lg"><p class="text-gray-300 text-center">#Messi</p></div>
   <div class="bg-gray-600 mt-2 rounded-lg"><p class="text-gray-300 text-center">#Messi</p></div>

   <div class="mt-12"> <h1 class="text-gray-300 text-xl text-center"> Mensajes directos </h1></div>

   <div @click="doClickMaestroSplinter(0)" class="grid grid-cols-2 bg-gray-600 rounded-md mt-1 p-2">
      <div class="bg-[url('https://pbs.twimg.com/profile_images/1722501239450021888/oYy45eaU_400x400.jpg')] bg-cover w-12 h-12 rounded-full mt-3"></div>
      <div class="mt-3"> <p class="text-gray-300">Marco Perez</p> <p class="text-gray-300 text-sm">Hace 10 minutos</p></div>
   </div>

   <div @click="doClickMaestroSplinter(1)" class="grid grid-cols-2 bg-gray-600 rounded-md mt-4 p-2">
     <div class="bg-[url('https://pbs.twimg.com/profile_images/1551642306616463364/3spZpRia_200x200.jpg')] bg-cover w-12 h-12 rounded-full mt-3"></div>
     <div><p class="text-gray-300">Juanito Alimaña</p> <p class="text-gray-300 text-sm">Ayer</p></div>
   </div>
   <div>
   </div>
  </div>

  <div class="p-2">
    <div class="text-gray-300 text-xl">{{ mensajes[index].name }}</div>
    <div class="bg-gray-900 rounded-lg w-72 h-20 p-4 mt-6 border border-slate-400">
      <div><h1 class="text-gray-300 ">{{ mensajes[index].mensaje1 }}</h1></div>
      <div><p class="text-slate-700 flex justify-end">25/06/2009 10:50 AM</p></div>
    </div>

    <div class="bg-gray-900 border border-slate-400 mt-6 rounded-lg w-72 h-20">
      <div> <h1 class="text-gray-300 mt-3 ml-3"> {{mensajes[index].mensaje2 }}</h1></div>
      <div class="flex justify-end mt-2 mr-3 text-slate-700"> 25/06/2009 10:50 AM </div>
    </div>

    <div class="bg-gray-900 border border-slate-400 mt-6 rounded-lg w-72 h-24">
    <div> <h1 class="text-gray-300 mt-3 ml-3"> {{ mensajes[index].mensaje3 }} </h1></div>
    <div class=" flex justify-end mt-2 mr-3 text-slate-700 "> 25/06/2009 10:50 AM </div>
    </div>
  </div>



  <div class="bg-gray-800 rounded-sm p-2">

  <div class="text-gray-300 text-center text-xl font-medium">PUBLICIDAD</div>
  
  <div class="bg-[url('https://i.ytimg.com/vi/aw1QFNSn5uM/maxresdefault.jpg')] bg-cover h-48 w-48 rounded-md mx-auto mt-4"></div>

  <div class="bg-[url('https://assets.change.org/photos/3/ub/eh/DKuBeHdNCEOQcyR-1600x900-noPad.jpg?1565970697')] bg-cover h-48 w-48 rounded-md mt-4 mx-auto"></div>
  </div>
</div>
</template>


