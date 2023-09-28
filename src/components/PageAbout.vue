<template>
  <div class="About">
    <div class="page_container">
      <p class="page_title">About Me</p>

      <div class="page_purpose">
        <p>사용자를 위한 개발자</p>
        
      </div>

      <div class="page_detail">
        <p>저는 아이디어를 구현하기 위해 개발을 시작했습니다.<br/> 이후 여러 프로젝트에 참여하며 아이디어를 직접 개발하며 서비스의 흐름을 체득하려고 노력하였습니다.<br/>
          계속해서 사용자를 위한 서비스를 제공하기 위해 프로그램을 개발하는 개발자가 되겠습니다.</p>
      </div>
    </div>
  </div>
</template>

<script>
  export default {}
</script>

<style lang="scss" scoped>
  @media (min-width: 801px) {
    .About {
      width: 100%;
      box-sizing: border-box;
      padding-left: 7%;
      color: var(--default-color);

      .page_container {
        margin: auto;
        padding-bottom: 100px;
        font-size: 72px;
        text-align: left;

        .page_title {
          margin: 92px 0px 0px 0px;
          display: inline-block;
          position: relative;
          font-weight: bold;
          letter-spacing: 2.16px;
        }

        .page_title:after {
          content: '';
          width: 147px;
          position: absolute;
          left: 0;
          bottom: -11px;
          border-width: 0 0 6px;
          border-style: solid;
        }

        .page_purpose {
          margin: 88px 0px 0px 0px;
          font-size: 32px;
          color: #232323;
        }

        .page_detail {
          margin: 43px 0px 0px 0px;
          font-size: 24px;
          color: #232323;
        }
      }
    }
  }

  @media (max-width: 800px) {
    .About {
      width: 100%;
      color: var(--default-color);

      .page_container {
        padding-bottom: 50px;

        .page_title {
          position: relative;
          padding-top: 50px;
          margin: 0% 0% 0% 8%;
          font-weight: bold;
          font-size: 36px;
        }

        .page_title:after {
          content: '';
          width: 101px;
          position: absolute;
          left: 0;
          bottom: -11px;
          border-width: 0 0 6px;
          border-style: solid;
        }

        .page_purpose {
          margin: 8% 0% 0% 8%;
          font-size: 24px;
          color: #232323;
        }

        .page_detail {
          margin: 8% 0% 0% 8%;
          font-size: 16px;
          color: #232323;
        }
      }
    }
  }
</style>
