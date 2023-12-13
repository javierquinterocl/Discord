<script setup>
const props = defineProps({
  hutao: [],
  seven: [],
  bronya: []
})
const emits = defineEmits(['valueUser'])

function valueUser(index) {
  emits('valueUser',index)
}
</script>

<template>
  <div class="flex mt-12">
    <div class="flex flex-col pl-6">
      <span class="text-zinc-300 text-xl">MENSAJES DIRECTOS</span>
      <div class="flex flex-col space-y-2">
        <div
          class="flex mt-6 bg-zinc-600 w-80 py-2 rounded pl-6 cursor-pointer"
          @click="valueUser(props.hutao)"
        >
          <img
            class="w-10 rounded-[100%]"
            src="https://i.pinimg.com/564x/12/31/4a/12314acaa96355c5b3980754af1db379.jpg"
            alt=""
          />
          <div class="flex flex-col pl-4">
            <span class="text-sm text-zinc-200">Hu Tao</span>
            <span class="text-xs text-zinc-400">Hace 10 minutos</span>
          </div>
        </div>
        <div
          class="flex mt-6 bg-zinc-600 w-80 py-2 rounded pl-6 cursor-pointer"
          @click="valueUser(props.seven)"
        >
          <img
            class="w-10 rounded-[100%]"
            src="https://i.pinimg.com/originals/81/1a/8a/811a8ac9998743ac8f958f650111bea3.jpg"
            alt=""
          />
          <div class="flex flex-col pl-4">
            <span class="text-sm text-zinc-200">7 de Marzo</span>
            <span class="text-xs text-zinc-400">En linea</span>
          </div>
        </div>
        <div
          class="flex mt-6 bg-zinc-600 w-80 py-2 rounded pl-6 cursor-pointer"
          @click="valueUser(props.bronya)"
        >
          <img
            class="w-10 rounded-[100%]"
            src="https://i.pinimg.com/474x/7d/71/c9/7d71c9fe1cf1d0c68acc3b9cfa5cbea3.jpg"
            alt=""
          />
          <div class="flex flex-col pl-4">
            <span class="text-sm text-zinc-200">Bronya</span>
            <span class="text-xs text-zinc-400">Hace 24 minutos</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
