<template>
          
         <nav class="bg-gray-800 text-white py-6 pb-6">
           <h1 class="pl-4 text-6xl font-medium text-center">FELIPE CORREIA - Programador Unity </h1>
         </nav>

         <!-- Linha horizontal -->
        

         <div class="text-center pr-10 pt-12">
           <h1 class="text-5xl text-gray-600 font-thin pb-6 pt-10 text-center ">Sobre</h1>
           <div class="flex justify-center">
            <div class="w-56 h-64 overflow-hidden rounded-xl mr-6 ml-4 ">
              <img class=" size-96 object-cover pb-20" src="/src/img/ProfilePortfolio.png" alt="">
            </div>
            <div class="w-1/2 text-left pl-6 pr-10 pt-14"> 
              <p class="font-thin text-lg">Programador <strong>Unity/C#</strong> recém-formado em Jogos Digitais, com a motivação de um gamer apaixonado. Além de programação, já participei de projetos na área de <strong>Modelagem</strong>, tanto de personagens quanto de outros objetos. Também como artista técnico, criando efeitos visuais como shader de água e <strong>CellShading</strong> na Unity. Tenho sempre curiosidade e vontade de entender as áreas relacionadas ao desenvolvimento de jogos.</p>
            </div>
           </div>
         </div>
         
         <!-- Linha horizontal -->
         <div class="w-3/4 h-0.5 bg-gray-300 mx-auto my-4 mt-20"></div>

         <div class="text-center pr-10 pt-6">
          <h1 class="text-5xl text-gray-600 font-thin pb-6 pt-10 text-center ">Jogos</h1>

          <!-- Grid Layout -->
          <div class="grid grid-cols-3 gap-8 px-20 mt-10">
            <!-- Grid Item 1 -->
            <div class="bg-white rounded-lg shadow-lg overflow-hidden">
               <div class="aspect-video">

                <iframe 
                :src="jorginhourl" 
                title="Player de vídeo do YouTube" 
                frameborder="0" 
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                allowfullscreen
                class="w-full h-full rounded-lg shadow-md">
              </iframe>
              </div>
             <!-- <img src="/path/to/your/image1.jpg" alt="Game 1" class="w-full h-48 object-cover"> -->
              <div class="p-4">
                <h3 class="text-xl font-semibold text-gray-800">As aventuras de Jorginho</h3>
                <p class="text-gray-600 mt-2">Primeiro jogo desenvolvido na faculdade utilizando WindowsForms e agora refeito em Unity.</p>
                <p class="text-gray-600 mt-2 text-center">Nesse projeto, fui o único programador, responsável por toda a lógica do jogo e implementação de funcionalidades, Enquanto a arte foi responsabilidade de outro integrante do grupo</p>
               <div class="w-3/4 h-0.5 bg-gray-300 mx-auto my-4 mt-6"></div>
                <p class="text-gray-600 mt-2 text-center">Link: <a class="hover:text-blue-600 " href="https://felipecg.itch.io/as-aventuras-de-jorginho" target="_blank" rel="noopener noreferrer">As aventuras de Jorginho - Itch.io</a> </p>
              </div>
            </div>

            <!-- Grid Item 2 -->
            <div class="bg-white rounded-lg shadow-lg overflow-hidden">
              <div class="aspect-video">

                <iframe 
                :src="memorizelibrasUrl" 
                title="Player de vídeo do YouTube" 
                frameborder="0" 
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                allowfullscreen
                class="w-full h-full rounded-lg shadow-md">
              </iframe>
              </div>
             <!-- <img src="/path/to/your/image2.jpg" alt="Game 2" class="w-full h-48 object-cover">-->
              <div class="p-4">
                <h3 class="text-xl font-semibold text-gray-800">Memorize Libras</h3>
                <p class="text-gray-600 mt-2">Jogo desenvolvido para a faculdade, com intuito de ensinar a Língua Brasileira de Sinais (Libras) de forma interativa para crianças.</p>
                <p class="text-gray-600 mt-2 text-center">Nesse projeto, fui o programador responsável por toda a lógica do jogo e implementação de funcionalidades. Incluindo a acessibilidade presente com o uso do Vlibras.</p>
               <div class="w-3/4 h-0.5 bg-gray-300 mx-auto my-4 mt-6"></div>
                <p class="text-gray-600 mt-2 text-center" > Link: <a href="https://felipecg.itch.io/memorize-libras-zoo" class="hover:text-blue-600" target="_blank" rel="noopener noreferrer">Memorize Libras - Itch.io</a></p>
              </div>
            </div>

            <!-- Grid Item 3 -->
            <div class="bg-white rounded-lg shadow-lg overflow-hidden">
              <div class="aspect-video">

                <iframe 
                :src="videoFileUrl" 
                title="Player de vídeo do YouTube" 
                frameborder="0" 
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                allowfullscreen
                class="w-full h-full rounded-lg shadow-md">
              </iframe>
              </div>
             <!-- <img src="/path/to/your/image3.jpg" alt="Game 3" class="w-full h-48 object-cover"> -->
              <div class="p-4">
                <h3 class="text-xl font-semibold text-gray-800">Tekhno</h3>
                <p class="text-gray-600 mt-2">Jogo desenvolvido para a faculdade durante o 4° semestre.</p>
                <p class="text-gray-600 mt-2">Projeto em equipe de 3 pessoas, onde atuei como programador Unity/C#, desenvolvendo as mecânicas de jogo e implementando sistemas de interação, como sistema de cutscenes utilizando o Timeline.</p>
              </div>
            </div>
          </div>

         

          <div class=" pt-40 bg-white rounded-lg shadow-lg overflow-hidden">
         </div> 
        </div>



         <footer class="bg-gray-800 text-white py-6 pt-4">
           <div class="container mx-auto text-center">
             <p>&copy; 2023 Felipe Correia. Todos os direitos reservados.</p>
           </div>
         </footer>

</template>

<script  setup>
import { ref } from 'vue'
import NavbarComponent from './components/NavbarComponent.vue';
import PopUpComponent from './components/PopUpComponent.vue';
import ButtonPopUp from './components/ButtonPopUp.vue';
import DropdownComponent from './components/DropdownComponent.vue';

const videoFileUrl = ref('https://www.youtube.com/embed/X-1WJYfAfxY')
const memorizelibrasUrl = ref('https://www.youtube.com/embed/gRFNGsfl_0g')
const jorginhourl = ref('https://www.youtube.com/embed/R9Julk2VI7c')


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
