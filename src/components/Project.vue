<template>
  <div class="project">
    <div class="project_container">
      <p class="project_top">Project</p>

      <div class="project_list">
        <div class="project_item" v-for="project in projectList" :key="project.id">
          <img :src="project.image" />
          <p class="project_title">{{ project.title }}</p>
          <p class="project_content">{{ project.content }}</p>
          <p class="project_language">{{ project.language }}</p>
          <p class="project_date">{{ project.date }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        projectList: [
          {
            image: require('./../assets/carFixer.png'),
            title: '차량 파손 검출 및 견적 비교 커뮤니티',
            content: '사용자가 차량 사진을 대량으로 업로드하면 파손 결과를 알려줍니다. 그리고 사용자가 수리비를 업로드하면, 다른 사용자들과 비교가 가능한 웹사이트입니다.',
            language: '사용 언어 : HTML, PHP, CSS, Python(FLASK), MySQL',
            date: '제작 기간 : 2022 . 04 ~ 2022 . 06',
          },
          {
            image: require('./../assets/book_review.png'),
            title: '서평 웹사이트',
            content: '사용자들이 서평을 자유롭게 업로드하고, 의견을 나눌 수 있는 반응형 웹사이트입니다.',
            language: '사용 언어 : HTML, PHP, CSS, MySQL',
            date: '제작 기간 : 2020 . 10 ~ 2020 . 12',
          },
          {
            image: require('./../assets/hotel_site.png'),
            title: '호텔 웹사이트',
            content: '호텔 예약 및 예약 확인이 가능한 사이트입니다.',
            language: '사용 언어 : VUE, Node.js, Javascript',
            date: '제작 기간 : 2020 . 09 ~ 2020 . 10',
          },
          {
            image: require('./../assets/EB_Library.png'),
            title: '도서관 웹사이트',
            content: '도서관 사이트이며, 도서 검색, 회원 관리, 커뮤니티 기능 등이 있습니다. 운영자, 사용자로 권한을 조정하여 기능을 이용할 수 있는 웹사이트입니다.',
            language: '사용 언어 : HTML, PHP, CSS, MySQL',
            date: '제작 기간 : 2020 . 04 ~ 2020 . 06',
          },
          {
            image: require('./../assets/portfolio.png'),
            title: '포트폴리오 사이트',
            content: '해당 포트폴리오 사이트입니다.',
            language: '사용 언어 : VUE, Node.js',
            date: '제작 기간 : 2020 . 03 ~ 2020 . 04',
          },
          {
            image: require('./../assets/awards_1.png'),
            title: '(KYIC)대한민국 청소년 발명 아이디어 경진대회',
            content: '금상',
            date: '2017 . 04 ~ 2017 . 05',
          },
          {
            image: require('./../assets/awards_2.png'),
            title: '독립기념관 혁신 아이디어 공모전',
            content: '아이디어상',
            date: '2019 . 06 ~ 2019 . 07',
          },
          {
            image: require('./../assets/kt_aivle.png'),
            title: 'KT AIVLE SCHOOL',
            content: '부트캠프를 참여하여 AI 및 데이터 분석 프로젝트를 수행하고 있습니다.',
            date: '2023 . 08 ~ 2024 . 01',
          },
        ],
      }
    },
  }
</script>

<style lang="scss" scoped>
  @media (min-width: 800px) {
    .project {
      width: 100%;
      background: #827c7c;
      color: var(--title-color);

      .project_container {
        width: 1100px;
        margin: auto;
        padding-bottom: 100px;
        font-size: 72px;
        text-align: left;

        .project_top {
          margin: 92px 0px 0px 0%;
          display: inline-block;
          font-weight: bold;
          position: relative;
          
        }

        .project_top:after {
          content: '';
          width: 163px;
          position: absolute;
          left: 0;
          bottom: -14px;
          border-width: 0 0 6px;
          border-style: solid;
        }

        .project_list {
          display: flex;
          justify-content: space-between;
          flex-wrap: wrap;

          .project_item {
            width: 45%;
            margin-left: 5%;
            margin-top: 100px;
            display: inline-block;

            img {
              width: 90%;
              margin: 0px;
            }

            .project_title {
              margin: 10px 0% 40px 0px;
              font-weight: 580;
              font-size: 38px;
            }

            .project_content {
              margin: 4px 10% 0px 0px;
              font-size: 29px;
              word-break: break-all;
              // color: #d8cdb5e1;
              color: #c5c4c2e1;
            }
            .project_language {
              margin: 25px 0px 10px 0px;
              font-size: 25px;
              color: #171414;
            }

            .project_date {
              margin: 25px 0px 0px 0px;
              font-size: 25px;
              color: #171414;
            }
          }
        }
      }
    }
  }
  @media (max-width: 800px) {
    .project {
      width: 100%;
      background: #827c7c;
      color: var(--title-color);

      .project_container {
        padding-bottom: 50px;
        font-size: 24px;
        text-align: left;

        .project_top {
          margin: 0% 0% 0% 8%;
          padding-top: 50px;
          font-size: 36px;
          font-weight: bold;
          position: relative;
        }

        .project_top:after {
          content: '';
          width: 120px;
          position: absolute;
          left: 0;
          bottom: -14px;
          border-width: 0 0 6px;
          border-style: solid;
        }

        .project_list {
          display: flex;
          justify-content: space-between;
          flex-wrap: wrap;

          .project_item {
            width: 80%;
            margin-top: 50px;
            margin-left: 10%;
            display: inline-block;

            img {
              width: 100%;
              margin: 0px;
            }

            .project_title {
              margin: 10px 0px 0px 0px;
              font-weight: 500;
              font-size: 24px;
            }

            .project_content {
              margin: 4px 0px 0px 0px;
              font-size: 16px;
              word-break: break-all;
              
              color: #c5c4c2e1;
            }
            .project_language {
              margin: 25px 0px 10px 0px;
              font-size: 16px;
              color: #171414;
            }

            .project_date {
              margin: 25px 0px 0px 0px;
              font-size: 16px;
              color: #110505;
            }
          }
        }
      }
    }
  }
</style>
