<template>
  <q-page class="xs:bg-white sm:bg-green md:bg-blue lg:bg-red xl:bg-orange ">
    <div class="hello w-full text-center">
      <h1 class="w-full font-serif text-5xl text-black bg-green border-red-dark font-extrabold text-center">Tailwindcss Demo</h1>
      <div class="w-full min-h-screen bg-blue-light">
        <h3>TailWind 配置使用</h3>
        <p class="text-22"><span class="font-bold">NO.1:</span><span>有新的css样式配置更改时在tailwind.js配置中添加对应的样式，然后运行npm run build:tw</span></p>
        <p class="text-18"><span class="font-bold">NO.2:</span><span>如果和quasar一起使用，担心被quasar样式覆盖，可通过tailwind.js &rArr; options &rArr; important:true（不过一般不建议这么使用，应尽量避免过多使用important）</span></p>
        <p class="text-18"><span class="font-bold">NO.3:</span><span>修改增加css样式配置举例:设置一个最大宽度1200px&rArr; tailwind.js &rArr; maxWidth &rArr;添加 '1200': '1200px'  &rArr; 使用时添加类名max-w-1200即可</span></p>
      </div>
      <div class="flex flex-wrap w-full justify-between px-8 py-4 bg-grey-dark">
        <div class="max-w-sm rounded overflow-hidden shadow-lg bg-white ml-4">
          <img class="w-full" src="https://www.tailwindcss.cn/img/card-top.jpg" alt="Sunset in the mountains">
          <div class="px-6 py-4">
            <div class="font-extrabold font-sans text-3xl leading-loose underline mb-2 select-text tracking-tight">The Coldest Sunset</div>
            <p class="font-serif font-bold text-grey-darker text-2xl leading-tight tracking-wide select-none truncate">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil.
            </p>
          </div>
          <div class="px-6 py-4">
            <span class="inline-block bg-grey-lighter rounded-full px-3 py-1 text-xl font-mono font-semibold text-grey-darker uppercase mr-2 align-bottom">#photography</span>
            <span class="inline-block bg-grey-lighter rounded-full px-3 py-1 text-sm font-mono font-light text-grey-darker line-through mr-2">#travel</span>
            <span class="inline-block bg-grey-lighter rounded-full px-3 py-1 text-sm font-mono font-thin text-grey-darker">#winter</span>
          </div>
        </div>
        <div class="bg-white h-32 ml-8 mt-4 px-4 flex justify-center items-center border-4 border-dashed border-black border-b-0 rounded-lg">
          <div class="w-16 h-16 bg-green"></div>
          <div class="w-16 h-16 bg-red"></div>
          <div class="w-16 h-16 bg-blue"></div>
          <div class="w-16 h-16 bg-orange"></div>
        </div>
        <div class="bg-white w-64 h-64 ml-8 mt-4 px-4 py-4 flex justify-between  border-2 border-dotted border-blue-darker border-t-0 rounded">
          <div class="w-16 h-16 bg-green"></div>
          <div class="w-16 h-16 bg-red"></div>
          <div class="w-16 h-16 bg-blue"></div>
          <div class="w-16 h-16 bg-orange"></div>
        </div>
        <div class="bg-white w-64 h-48 ml-8 mt-4 px-4 border-4 border-dotted border-black rounded-lg rounded-r-none">
          <div class="w-16 h-16 bg-green inline-block"></div>
          <div class="w-16 h-16 bg-red inline-block mx-4"></div>
          <div class="w-16 h-16 bg-blue block"></div>
        </div>
        <div class="bg-white w-64 h-32 ml-8 mt-4 clearfix border-4 border-solid border-red rounded-lg rounded-l-none">
          <div class="w-16 h-16 bg-green float-left"></div>
          <div class="w-16 h-16 bg-red float-left"></div>
          <div class="w-16 h-16 bg-blue float-right"></div>
        </div>
        <div class="bg-white w-64 h-32 ml-8 mt-4 flex flex-no-wrap">
          <div class="w-16 h-16 bg-green flex-none"></div>
          <div class="w-16 h-16 bg-red flex-none"></div>
          <div class="w-16 h-16 bg-blue flex-none"></div>
          <div class="w-16 h-16 bg-blue flex-none"></div>
          <div class="w-16 h-16 bg-blue flex-none"></div>
        </div>
        <div class="w-64 h-64 no-repeat bg-auto" :style="imgClass('https://www.tailwindcss.cn/img/card-top.jpg')">
        </div>
        <div class="w-64 h-64 no-repeat bg-cover bg-top" :style="imgClass('https://www.tailwindcss.cn/img/card-top.jpg')">
        </div>
        <div class="w-64 h-64 no-repeat bg-contain bg-left-bottom" :style="imgClass('https://www.tailwindcss.cn/img/card-top.jpg')">
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
// import '@/css/tailwind/index'

export default {
  name: 'PageIndex',
  components: {},
  data () {
    return {}
  },
  methods: {
    imgClass (img) {
      return {
        backgroundImage: `url(${img})`
      }
    }
  }
}
</script>

<style lang="sass" scoped>

</style>
