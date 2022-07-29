<template>
  <div class="container mt-5">
    <div class="circle-1 w-20 h-20 absolute top-30 left-30 rounded-full bg-gradient-to-r from-yellow-200 to-amber-400"></div>
    <div class="circle-2 w-30 h-30 absolute bottom-30 right-30 <sm:right-50 rounded-full bg-gradient-to-r from-red-200 to-pink-400"></div>
    <div class="circle-3 w-20 h-20 absolute top-50 right-80 <sm:right-10 bg-gradient-to-r from-cyan-500 to-blue-500" style="border-radius: 30% 70% 67% 33% / 45% 56% 44% 55%"></div>
    <div class="circle-3 w-20 h-20 absolute bottom-50 left-2/3 bg-gradient-to-r from-purple-200 to-violet-500" style="border-radius: 57% 43% 51% 49% / 46% 27% 73% 54%"></div>

    <div class="content inset-center ">
      <div class="overflow-hidden md:w-[600px] <md:w-[600px] sm:w-[350px] <sm:w-[350px] h-[80px] m-0 p-0">
        <div class="h-full flex items-center mr-3 float-left">
          <p class="inline text-[32px] <sm:text-[22px] font-semibold text-[#41b883]">Nuxt3</p>
        </div>
        <ul class="start-text">
          <li v-for="(item, i) in features" :key="i"
              class="text-sky-600 font-semibold"
              :class="[
                  i  === 0 ? 'text-emerald-600' :
                  i  === 1 ? 'text-teal-600' :
                  i === 2 ? 'text-cyan-600' :
                  i === 3 ? 'text-sky-600' : ''
              ]"
          >{{ item }}️️</li>
        </ul>
      </div>
      <div class="flex items-center gap-5 mt-5">
        <Anchor
            href="https://v3.nuxtjs.org/"
            title="Github"
        >
          <Button>
            <IconLogos:nuxt-icon class="w-5 h-5 mr-2"/>
            Nuxt 3
          </Button>
        </Anchor>
        <Anchor
            href="https://github.com/tuongmengleang/nuxt3-boilerplate"
            title="Github"
        >
          <Button color="secondary">
            <IconLogos:github-icon class="w-5 h-5 mr-2"/>
            Github
          </Button>
        </Anchor>

      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>

definePageMeta({
  layout: 'page',
})

const features: [string, string, string, string] = [
    "Lighter ⚡",
    "Faster 💨",
    "Universal 🪐",
    "Awesome 🔥"
]

</script>

<style lang="scss" scoped>
.start-text {
  @apply block text-[60px] md:text-[44px] <md:text-[44px] sm:text-[30px] <sm:text-[30px] overflow-hidden mt-0 text-left;
  animation-name: change;
  animation-duration: 10s;
  animation-iteration-count: infinite;
  li {
    display: block;
    padding: 15px 0;
    line-height: 52px;
  }
}
@keyframes opacity {
  0%, 100% {opacity:0;}
  50% {opacity:1;}
}

@keyframes change {
  0%, 12.66%, 100% {transform:translate3d(0,0,0);}
  16.66%, 29.32% {transform:translate3d(0,-25%,0);}
  33.32%,45.98% {transform:translate3d(0,-50%,0);}
  49.98%,62.64% {transform:translate3d(0,-75%,0);}
  66.64%,79.3% {transform:translate3d(0,-50%,0);}
  83.3%,95.96% {transform:translate3d(0,-25%,0);}
}
</style>
