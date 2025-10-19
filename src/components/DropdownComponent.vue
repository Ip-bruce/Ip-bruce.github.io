<template>
  
  <mask v-show="isOpen" @click="close" class=" cursor-pointer z-10 w-full absolute  h-screen top-0 left-0 flex justify-center " >
    
  </mask>
    <div v-show="true" @click.stop ref="root" class=" cursor-default relative inline-block text-left cursor-default">
      <button
    type="button"
    class="px-3 py-1 mt-1 bg-white border rounded shadow-sm text-sm hover:bg-gray-50 ring-1 ring-black ring-opacity-10 "
    @click="toggle"
    :aria-expanded="isOpen.toString()"
    aria-haspopup="true"
    >
    <slot name="button">{{ title }}</slot>
  </button>
  
  <transition name="fade">
    <div
    v-show="isOpen"
    class="origin-top-right absolute right-0 mt-2 w-20 rounded-md shadow-lg bg-white ring-1 ring-black ring-opacity-10 z-20"
    role="menu"
    >
    <div>
      <slot @click="close" >
        <!-- default dropdown content -->
        <div class="px-4  text-sm text-gray-700">No items</div>
      </slot>
    </div>
  </div>
</transition>
</div>
</template>

<script setup>
import { ref,  } from 'vue'

const props = defineProps({
  title: { type: String, default: '⁝' }
})

const root = ref(null)
const isOpen = ref(false)

function open() {
  isOpen.value = true
}
function close() {
  isOpen.value = false
}
function toggle() {
  isOpen.value = !isOpen.value
}


defineExpose({ open, close, toggle })
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 150ms ease, transform 150ms ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
  transform: translateY(-4px);
}
.fade-enter-to,
.fade-leave-from {
  opacity: 1;
  transform: translateY(0);
}
</style>
