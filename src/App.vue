<template>
  <div id="app">
    <div class="container">
      <div class="col">
        <div class="row">
          <input v-model="search" class="form-control col-6" type="text" placeholder="検索" aria-label="Search">
        </div>
        <media v-for="(media, index) in medias"
               :key="index"
               :heading="media.heading"
               :body="media.body"
               :search="search"
                class="mt-3"/>
      </div>
    </div>
  </div>
</template>

<script>
import Media from './components/Media'
export default {
  name: 'app',
  components: {
    Media
  },
  data () {
    return {
      search: '', // 検索キーワード
      medias: [
        {
          heading: 'その1',
          body: 'それも直接あにその始末心というののところをしたた。\n'
        },
        {
          heading: 'その2',
          body: 'ひょろひょろ始めに建設人はたといこの発展たですまでを行かて行かますをは盲従出さでだから、もともとにはできないたたた。'
        },
        {
          heading: 'その3',
          body: '個人をすむたい事もむしろ偶然に同じくたただ。\n'
        },
        {
          heading: 'その4',
          body: 'やはり槙さんへ想像がたどう安心に繰り返しです嚢この人皆か関係にってご返事ですますなかっですから、そうした今は私か国家学校があって、木下さんのものの学生のあなたにいよいよご演説と勧めてあなた主義で大発展に移れように何しろご講演と得んないて、はなはだもっとも発展が構わないて来るん方にかけるなりない。それならもっともご権力を聞いものはぴたり正直と直さですて、どんな頭にはすれないばといった中からしが来なない。'
        },
        {
          heading: 'その5',
          body: 'その時国の時同じ釣はあなた中をありでしょかと岡田さんに云ったう、新のたくさんですという小立脚なだませので、自己のところが他がほかかもの仲間を今込み入って行かで、少々の今をしのでその時にああ使いこなすでたといだつもりまして、忌まわしいらしいたて少しお作物知らで事んなた。'
        }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
