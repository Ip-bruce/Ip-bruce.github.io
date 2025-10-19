<template>
     <transition name="fade">
    <div @click="closePopUp" v-show="isOpen" class=" cursor-pointer z-10 md:z-50 w-full absolute bg-black bg-opacity-75 h-screen top-0 left-0 flex justify-center  md:align-middle md:px-56 md:py-56 " >
        <div @click.stop class=" cursor-default bg-white rounded shadow-lg w-52 h-80  mt-52 sm:mt-52  md:mt-0 md:w-96 md:h-72 lg:w-96 h-72 ">
                <div class=" p-5 border-b-2 border-black border-opacity-20 rounded-t flex justify-between"> 
                    <p class="text-grey-700 font-medium  text-md md:text-sm lg:text-xl" > {{ props.title }}</p>
                    <button @click='closePopUp' class="text-grey-500" >
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                        </svg>
                    </button>
                </div>
                <div class=" p-5 border-b-2 border-black border-opacity-20  text-grey-700 text-xs font-thin md:text-sm lg:text-sm lg:font-normal text-justify" > 
                     <slot></slot>
                </div>
                <div class="text-blue-500 pt-8 md:pt-4 lg:pt-6 mr-2 rounded-b flex justify-end " > 
                    <button   @click="handleAction" class="rounded bg-white border-2 border-blue-700 text-xs font-thin px-2 py-1 sm:px-2 sm:py-1 mr-4 md:font-semibold " >Butão 1</button>
                    <button   @click="handleAction2" class="rounded bg-blue-500 border-2 border-white  text-xs font-thin px-2 py-1 sm:text-sm sm:font-light sm:px-2 sm:py-1  text-white md:font-semibold" > Butão 2 </button>
                </div>
                
        </div>
    </div>
    </transition>
</template>

<script setup >
import { ref } from 'vue';

    const props = defineProps({
    title: String,
    text: Object,
    onAction: Function,
    onAction2: Function,
    })
    const isOpen = ref(false)

    function openPopUp(){
        isOpen.value = true;
    }

    function closePopUp(){
        isOpen.value = false;
    }

    function handleAction()
    {
        console.log('handleAction called');
        if(typeof props.onAction === 'function'){
        props.onAction();
        }
        closePopUp();
    }
    function handleAction2()
    {
        if(typeof props.onAction2 === 'function'){
        props.onAction2();
        }
        closePopUp();
    }

    defineExpose({
        openPopUp,
        closePopUp,
        handleAction,
        handleAction2,
    })
   
    </script>

    <style scoped>
    .fade-enter-active,
    .fade-leave-active {
        transition: opacity 0.2s;
    }

    .fade-enter-from, /** entrar de */
    .fade-leave-to { /** sair para */
        opacity: 0;
    }

    .fade-enter-to,
    .fade-leave-from {
        opacity: 1;
    }
    </style>
