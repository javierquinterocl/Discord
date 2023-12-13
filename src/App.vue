<script setup>
import MensajeApp from '@/components/MensajeApp.vue'
import { ref } from 'vue'

const Hutao = ref([
  {
    mensaje: 'Hola como estas bebesita',
    fecha: '23/08/23 10:37 Am',
    name: 'Hu Tao'
  },
  {
    mensaje: 'Queria decirte que sos maquina',
    fecha: '23/08/23 10:38 Am',
    name: 'Hu Tao'
  },
  {
    mensaje: 'Un free?',
    fecha: '23/08/23 10:38 Am',
    name: 'Hu Tao'
  }
])
const seven = ref([
  {
    mensaje: 'Esto no es amor',
    fecha: '25/08/23 9:37 Pm',
    name: '7 March'
  },
  {
    mensaje: 'Lo que tu sientes',
    fecha: '23/08/23 9:39 Pm',
    name: '7 March'
  },
  {
    mensaje: 'Se llama obsesion',
    fecha: '23/08/23 10:38 Pm',
    name: '7 March'
  }
])
const bronya = ref([
  {
    mensaje: 'La vida se trata de perder',
    fecha: '27/08/23 01:37 Pm',
    name: 'Bronya'
  },
  {
    mensaje: 'Lograremos ganar algun dia?',
    fecha: '27/08/23 01:39 Am',
    name: 'Bronya'
  },
  {
    mensaje: 'Sea cual sea el resultado, habra mas batallas por luchar',
    fecha: '27/08/23 01:38 Pm',
    name: 'Bronya'
  }
])
const user = ref(Hutao.value)
function userChange(users) {
  user.value = users
}
</script>

<template>
  <div
    class="flex h-full bg-[url('https://c.wallhere.com/photos/af/d2/Discord_discordapp_discord_background-1278375.jpg!d')]"
  >
    <div class="flex mx-auto">
      <div class="bg-zinc-800 w-20 h-[100vh] flex flex-col">
        <div class="flex mx-auto mt-5">
          <div class="p-1 w-12 rounded-xl bg-white">
            <img
              class="w-12 rounded-full mx-auto"
              src="https://i.pinimg.com/136x136/56/2e/be/562ebed9cd49b9a09baa35eddfe86b00.jpg"
              alt=""
            />
          </div>
        </div>
        <span class="text-gray-400 text-xs text-center mt-2">Perfil</span>
      </div>
      <div class="bg-zinc-700 w-96 flex-col flex">
        <div class="flex mt-8">
          <div class="flex flex-col pl-6">
            <span class="text-zinc-300 text-xl">TENDENCIAS</span>
            <div class="mt-5 flex flex-col space-y-2">
              <span class="text-zinc-400">#Titanic</span>
              <span class="text-zinc-400">#Millonarios</span>
              <span class="text-zinc-400">#OcañaPonganBuenasLuces</span>
              <span class="text-zinc-400">#JavierCl</span>
              <span class="text-zinc-400">#KnivesOut</span>
              <span class="text-zinc-400">#ColombiaMArcha</span>
            </div>
          </div>
        </div>
        <MensajeApp :hutao="Hutao" :bronya="bronya" :seven="seven" @valueUser="userChange" />
      </div>
      <div class="bg-zinc-600 w-[500px] flex flex=col pl-6 relative">
        <div class="flex flex-col mt-8">
          <div class="">
            <span class="text-zinc-300 text-xl">{{ user[0].name }}</span>
            <div
              class="flex flex-col mt-6 bg-zinc-700 pl-2 py-2 w-[450px] pr-4 border border-zinc-400 rounded"
              v-for="(mensajes, index) in user"
              :key="index"
            >
              <span class="text-zinc-300">{{ mensajes.mensaje }}</span>
              <span class="text-zinc-400 text-sm justify-end flex mt-2">{{ mensajes.fecha }}</span>
            </div>
          </div>
        </div>
      </div>
      <div class="bg-zinc-900 w-72 flex flex-col">
        <div class="flex flex-col mt-8 pl-6 pr-6">
          <span class="text-zinc-300 text-xl">PUBLICIDAD</span>
          <div class="mt-4 flex flex-col rounded">
            <img
              class="rounded-xl"
              src="https://www.inboundcycle.com/hs-fs/hubfs/anuncios%20publicitarios%20recordatorios.jpg?width=480&height=600&name=anuncios%20publicitarios%20recordatorios.jpg"
              alt=""
            />
            <img
              class="mt-4 rounded-xl"
              src="https://inprofit.es/server/Portal_0033275/img/blogposts/spotify-ad-studio-publicidad-en-spotify_12107.png"
              alt=""
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
