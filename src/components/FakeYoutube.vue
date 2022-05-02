<template lang="pug">
div(class="header")
  img(src="../assets/ytlogo.jpg" class="float-left")
  img(src="../assets/member.jpg" class="float-right")
  img(src="../assets/search.jpg" class="search-img float-right")
  div(class="clearfix")
div(class="tag float-left" v-for="tag in tags") {{tag}}
div(class="clearfix")
div(class="grid lg:grid-cols-4 md:grid-cols-3  sm:grid-cols-1")
  div(class="video" v-for="video in videos")
    img(class="img" :src='video.img')
    img(class="author float-left" :src='video.author')
    div(class="video-info lg:float-right md:float-left md:contents")
      div(class="title font-bold") {{video.title}}
      div(class="detail text-slate-400") {{video.detail}}
    div(class="clearfix")
div(class="grid grid-cols-4")
  div(class="icon text-center	" v-for="icon in icons")
    img(class="" :src='icon.img')
    div(class="") {{icon.title}}

</template>

<script>
export default {
  name: 'FakeYoutube',
  data() {
    return{
      icons:[
        {
          title:"Home",
          img:require("@/assets/home_icon.jpg")
        },
        {
          title:"Trending",
          img:require("@/assets/trending_icon.jpg")
        },
        {
          title:"Subscription",
          img:require("@/assets/sub_icon.jpg")
        },
        {
          title:"Library",
          img:require("@/assets/lib_icon.jpg")
        }
      ],
      tags:[
        "All","Music","OnePiece","Anime"
      ],
      videos:[
        {
          title:"2021年最火的英文歌曲",
          img:"https://img.youtube.com/vi/VnAeWZZS6zo/hqdefault.jpg",
          author:"https://yt3.ggpht.com/ytc/AKedOLS_D7l0JFnzy9dIHhrhYJfviAhSR2_Za4-_XD05=s48-c-k-c0x00ffffff-no-rj",
          detail:"超好聽的英文歌 觀看次數：39萬次 直播時間：6 個月前"
        },
        {
          title:"2021年最火的英文歌曲",
          img:"https://img.youtube.com/vi/VnAeWZZS6zo/hqdefault.jpg",
          author:"https://yt3.ggpht.com/ytc/AKedOLS_D7l0JFnzy9dIHhrhYJfviAhSR2_Za4-_XD05=s48-c-k-c0x00ffffff-no-rj",
          detail:"超好聽的英文歌 觀看次數：39萬次 直播時間：6 個月前"
        },
        {
          title:"2021年最火的英文歌曲",
          img:"https://img.youtube.com/vi/VnAeWZZS6zo/hqdefault.jpg",
          author:"https://yt3.ggpht.com/ytc/AKedOLS_D7l0JFnzy9dIHhrhYJfviAhSR2_Za4-_XD05=s48-c-k-c0x00ffffff-no-rj",
          detail:"超好聽的英文歌 觀看次數：39萬次 直播時間：6 個月前"
        },
        {
          title:"2021年最火的英文歌曲",
          img:"https://img.youtube.com/vi/VnAeWZZS6zo/hqdefault.jpg",
          author:"https://yt3.ggpht.com/ytc/AKedOLS_D7l0JFnzy9dIHhrhYJfviAhSR2_Za4-_XD05=s48-c-k-c0x00ffffff-no-rj",
          detail:"超好聽的英文歌 觀看次數：39萬次 直播時間：6 個月前"
        },
        {
          title:"Billboard Hot 100 All Time 🪔🪔🪔 Adele, Maroon 5",
          img:"https://img.youtube.com/vi/9JDIZrQrw38/hqdefault.jpg",
          author:"https://yt3.ggpht.com/HzRAe6c8JbXuglTRScXmNB_jYDAYmbzAW0am2e4AydMxvWg7EpAmhatUCzutbyM8ifwHs2vn=s48-c-k-c0x00ffffff-no-rj",
          detail:"English Songs 觀看次數：390萬次 直播時間：8 個月前"
        },
        {
          title:"2021年最火的英文歌曲",
          img:"https://img.youtube.com/vi/VnAeWZZS6zo/hqdefault.jpg",
          author:"https://yt3.ggpht.com/ytc/AKedOLS_D7l0JFnzy9dIHhrhYJfviAhSR2_Za4-_XD05=s48-c-k-c0x00ffffff-no-rj",
          detail:"超好聽的英文歌 觀看次數：39萬次 直播時間：6 個月前"
        },
        {
          title:"2021年最火的英文歌曲",
          img:"https://img.youtube.com/vi/VnAeWZZS6zo/hqdefault.jpg",
          author:"https://yt3.ggpht.com/ytc/AKedOLS_D7l0JFnzy9dIHhrhYJfviAhSR2_Za4-_XD05=s48-c-k-c0x00ffffff-no-rj",
          detail:"超好聽的英文歌 觀看次數：39萬次 直播時間：6 個月前"
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .header{
    height: 50px;
    border-bottom: 2px gray solid;
    line-height: 50px;
    .search-img{
      height: 100%;
    }
  }
  .tag{
    border-radius: 20px;
    padding: 5px 10px;
    margin: 5px 5px;
    background-color: #e8e8e8;
  }
  .video{
    .author{
      border-radius: 99px;
    }
  }
  .icon{
    img{
      margin: 0 auto;
    }
  }
  .clearfix{
    clear: both;
  }
</style>
