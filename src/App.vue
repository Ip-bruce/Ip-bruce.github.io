<template>
          
          <nav class="w-full bg-blue-500 h-8 flex justify-between  " >
            <div class="text-white" >TITLE</div>
            <div class="flex justify-end" >
              <div class="text-white" >btn1</div>
              <div class="text-white" >btn2</div>
            </div>
          </nav>

          <div class=" flex justify-end align-middle " ref="root" >
          <DropdownComponent  >
            <div class="px-2 py-2 text-sm text-gray-700 hover:bg-gray-100 cursor-pointer" >Remover</div>
            <div class="px-2 py-2 text-sm text-gray-700 hover:bg-gray-100 cursor-pointer" >Editar</div>
            <div class="px-2 py-2 text-sm text-gray-700 hover:bg-gray-100 cursor-pointer" >Item 3</div>
          </DropdownComponent>
          </div>
          <div class="flex justify-center align-middle" >
            <ButtonPopUp @click="openPopUp()"></ButtonPopUp>
          </div>
          <PopUpComponent v-on:action2="textButton2" v-on:action="textButton" ref="popUp" title="Paralelepípedo" > Lorem ipsum, dolor sit amet consectetur adipisicing elit. Itaque fuga quam fugit architecto qui adipisci exercitationem inventore. Laboriosam placeat ea numquam, praesentium delectus accusamus nobis necessitatibus, explicabo debitis nihil magnam! </PopUpComponent>
          
          <!-- Teste função botão -->
          <div v-if="isReadable" class="flex justify-center  w-full ">
            <h1 class="font-extrabold text-orange-600" > Função do botao funcionou! </h1>
          </div>

</template>

<script  setup>
import { ref } from 'vue'
import PopUpComponent from './components/PopUpComponent.vue';
import ButtonPopUp from './components/ButtonPopUp.vue';
import DropdownComponent from './components/DropdownComponent.vue';



  const popUp = ref(null);

  const isReadable = ref(false);

  function openPopUp ()
  {
    popUp.value.openPopUp();
  } 

  function textButton()
  {
    isReadable.value = true;
  }
  function textButton2()
  {
    isReadable.value = false;
  }

 

</script>
