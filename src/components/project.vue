<template>
  <div class="part3">
    <div class="part3-container">
      <div class="part3-header">
        <div class="part3-title-container">
          <div class="title-bubble bubble1" />
          <div class="title-bubble bubble2" />
          <div class="title-font">
            我们推出了
          </div>
        </div>
        <div class="header-image" />
      </div>
      <div class="part3-body">
        <div
          v-for="(item,index) in projectCardInfo"
          :key="index"
          class="project-card"
        >

          <div class="project-card-header">
            <button 
              class="dianji" 
              @click="navToCardLink">
              在线演示
            </button>
            <div class="project-card-name">
              {{ item.cardTitle }}

            </div>

            <div
              class="project-detail"
              @click="navToCardLink(item)"
            >
              {{ item.cardIntro }}
            </div>
          </div>
          <div class="project-card-body" >
            <img
              :src="item.cardImage"
              alt
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: `Project`,
  data() {
    return {
      projectCardInfo: [
        {
          cardTitle: "「彩票娱乐城net综合盘」" ,
          cardIntro:
            "彩票娱乐城net综合盘。可以对接棋牌AG视讯，" +
            "包括个大平台开户." +
            "联系qq:532222521",

          cardImage:"https://cdn.guaiwola.com//yanshi/tianhang.png",
          navToCardLink:"http://cai1.a55a66.com"
        },
        {
          cardTitle: "「纯娱乐城net」",
          cardIntro:
            "百家乐棋牌娱乐城net综合盘。联系qq:532222521",

          cardImage: "http://ag.52miduo.com/uploads/20190115/ec8375f6883cbc6973eda1711b393159.png",
          navToCardLink:"http://cai1.a55a66.com"
        },
        {
          cardTitle: "「彩票娱乐城net综合盘」",
          cardIntro:
            "彩票娱乐城net综合盘。联系qq:532222521",

          cardImage: "http://ag.52miduo.com/uploads/20190115/82e4c966d29e4d235d77e993b6c161db.png",
          navToCardLink:"http://cai1.a55a66.com"
        },
        {
          cardTitle: "「彩票娱乐城net综合盘」",
          cardIntro:
            "彩票娱乐城net综合盘。联系qq:532222521",

          cardImage: "http://ag.52miduo.com/uploads/20190115/de7e36196a1e0efef74d1339bae91812.png",
          navToCardLink:"http://cai1.a55a66.com"
        },
        {
          cardTitle: "「彩票娱乐城net综合盘」",
          cardIntro:
            "彩票娱乐城net综合盘。联系qq:532222521",

          cardImage: "http://ag.52miduo.com/uploads/20190115/a1e888a64dcbe7b9c69a80abc2dc1543.png",
          navToCardLink:"http://cai1.a55a66.com"
        },
        {
          cardTitle: "「彩票娱乐城net综合盘」",
          cardIntro:
            "彩票娱乐城net综合盘。联系qq:532222521",

          cardImage: "http://ag.52miduo.com/uploads/20190115/5445548f445837382d7e38705d1ef4ef.png",
          navToCardLink:"http://cai1.a55a66.com"
        },
      ]
    };
  },
  methods: {
    navToCardLink({ navToCardLink }) {
      if (navToCardLink) {
        window.location.href = navToCardLink;
      }
    }
  }
};
</script>

<style lang="sass" scoped>
@import "../style/bubble.sass"
.z-top
  z-index: 1
.part3
  width: 100vw
  background-image: url('../assets/background/wave-line_3.svg')
  background-size: cover
  background-repeat: no-repeat
  display: flex
  justify-content: center
  background-position-y: -200px
  .part3-container
    width: 72%
    display: flex
    flex-direction: column
    align-items: center
    margin-bottom: 20px
    @media(max-width: $phone)
      width: 100%
    .part3-header
      width: 100%
      display: flex
      justify-content: space-between
      margin-bottom: 3.5rem
      align-items: center
      @media(max-width: $ipad)
        flex-direction: column
        align-items: flex-start
      @media(max-width: $phone)
        width: 72%
      .part3-title-container
        position: relative
      .title-font
        font-weight: 600
        font-size: 2.5rem
        @media(max-width: $phone)
          font-size: 1.5rem
          margin-bottom: 0.625rem
        color: #222222
      .header-image
        width: 33.75rem
        height: 26.0625rem
        background-size: 70%
        background-position: center
        background-repeat: no-repeat
        @media(max-width: $ipad)
          margin: auto
          background-size: 60%
        @media(max-width: $phone)
          width: 17.5rem
          height: 13.125rem
        background-image: url('https://static.airbob.org/homepage/xiaochenxu_1.png')
    .part3-body
      width: 100%
      display: grid
      grid-template-columns: repeat(2, 1fr)
      margin-bottom: 3.125rem
      @media(max-width: $ipad)
        grid-template-columns: repeat(1, 1fr)
        margin-bottom: 0
        justify-items: center
        width: 100vw
      .project-card
        color: red
        width: 28.75rem
        height: 21.5625rem
        border-radius: 10px
        position: relative
        cursor: pointer
        @media(min-width: $ipad)
          margin-bottom: 2.225rem
        @media(max-width: $ipad)
          margin-bottom: 4.375rem
        @media(max-width: $phone)
          margin-bottom: 5rem
          width: 17.5rem
          height: 13.125rem
        &:hover
          z-index: 1 // 保证hover到的card在顶层
          .project-card-header
            transform: translateY(-50%)
          .project-card-body
            box-shadow: 0 -5px 10px -4px rgba(0,0,0,0.20)
            transform: scale(1.1) translateY(20%)
        .project-card-header
          border-radius: 1rem;
          width: 100%
          height: auto
          transition: all 0.3s ease-out
          position: absolute
          top: 0
          background-color: #22b574
          color: #ffffff
          .dianji
              font-size: 0.875rem
              width: 5.75rem
              height: 2.2rem
              margin-right: 1.3125rem
              color: white
              outline: none
              border: none
              border-radius: 2.5rem
              text-decoration: none
              background: linear-gradient(to right, #8bd21f, #d8d23e)
              box-shadow: 0.125rem 0.25rem 0.3125rem #f3f6ac
              cursor: pointer
              margin: 10px -16px -42px 350px;
              &:active
                transform: translateY(0.1875rem)
                box-shadow: 0.125rem 0.125rem 0.3125rem #f3f6ac

          .project-card-name
            width: 299px;
            margin-left: 2.25rem
            padding-top: 1.5rem
            margin: -48px 0 0 0px;
            @media(min-width: $phone)
              font-size: 1.5rem

          .project-detail
            text-align: justify
            padding: 1.25rem
            margin: auto
            line-height: 1.25rem
            font-size: 90%
            @media(min-width: $phone)
              font-size: 1.125rem
              line-height: 1.5rem

        .project-card-body
          width: 100%
          height: auto
          border-radius: 10px
          position: absolute
          transition: all 0.3s ease-out
          top: 3.75rem
          background-color: #fafafa
          background-size: cover
          display: flex
          justify-content: center
          align-items: center
          img

            margin: auto
            width: 460px
            height: 256px
            border-radius: 10px

</style>

