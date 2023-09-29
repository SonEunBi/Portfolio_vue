<link href="https://cdn.jsdelivr.net/npm/animate.css@3.5.1" rel="stylesheet" type="text/css"></link>
<template>
  <div class="home_container">
    <div class="home_nav">
      <button v-for="menu in menuList" :key="menu.id" @click="move(menu)">{{ menu }}</button>
    </div>

    <div class="home_title">
      
      <p class="text"></p>
      <p class="text_bold" float=left;>Developer
      손은비 입니다</p>
      <p class ="text_blinking" float=left;>.</p>
    </div>

    <span class="author">Made by Son</span>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        menuList: ['Home', 'About', 'Skills', 'Project', 'Contact'],
      }
    },
    methods: {
      move(menu) {
        this.$emit('move', menu)
      },
    },
  }
</script>

<style lang="scss" scoped>
  @media (min-width: 801px) {
    .home_container {
      position: relative;
      width: 100%;
      height: 100%;
      background-image: url('../assets/img_bg.png');
      background-repeat: no-repeat;
      background-size: cover;

      .home_nav {
        display: flex;
        justify-content: flex-end;
        box-sizing: border-box;
        padding-top: 30px;
        padding-right: 180px;
        button {
          width: 80px;
          height: 30px;
          background-color: transparent;
          font-size: 18px;
          color: var(--title-color);
          &:hover {
            color: #bbbbbb;
          }
        }
      }
      @keyframes blink-effect {
  50% {
    opacity: 0;
    }
  }
      .home_title {
        position: absolute;
        top: 60%;
        left: 200px;
        color: var(--title-color);

        .text {
          font-size: 32px;
        }

        .text_bold {
          display:inline-block;
          font-size: 70px;
          font-weight: 500;
        }
        .text_blinking {
          display:inline-block;
          font-size: 70px;
          font-weight: 800;
          animation: blink-effect 1s step-end infinite;
        }
      }
      
      .author {
        position: absolute;
        left: 85%;
        top: 40%;
        color: var(--title-color);
        font-size: 24px;
        transform: rotate(0.25turn);
      }
    }
  }
  @media (max-width: 800px) {
    .home_container {
      position: relative;
      width: 100%;
      height: 100%;
      background-image: url('../assets/img_bg.png');
      background-repeat: no-repeat;
      background-size: cover;
      background-position: center;

      .home_nav {
        display: none;
      }
      @keyframes blink-effect {
  50% {
    opacity: 0;
    }
  }
      .home_title {
        position: absolute;
        top: 60%;
        left: 8%;
        color: var(--title-color);

        .text {
          font-size: 24px;
        }

        .text_bold {
          display:inline-block;
          margin-top: 25px;
          font-size: 36px;
          font-weight: 500;
        }
        .text_blinking {
          display:inline-block;
          font-size: 25px;
          font-weight: 800;
          animation: blink-effect 1s step-end infinite;
        }
      }

      .author {
        position: absolute;
        left: 80%;
        top: 20%;
        color: var(--title-color);
        font-size: 14px;
        transform: rotate(0.25turn);
      }
    }
  }
@media(max-width:800px){

}
</style>
