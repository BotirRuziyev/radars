<script>
import azimut from "@/assets/img/azimut.svg";
import elvis from "@/assets/img/elvis.svg";
import glonass from "@/assets/img/glonass.svg";
import almaz from "@/assets/img/almaz.svg";
import skba from "@/assets/img/skba.svg";
import rsai from "@/assets/img/rsai.svg";
import traced from "@/assets/img/traced.svg";

import navigator from "@/assets/img/navigator.svg";
import aviasia from "@/assets/img/aviasia.svg";
import spbgut from "@/assets/img/spbgut.svg";
import sogaz from "@/assets/img/sogaz.svg";
import konsern from "@/assets/img/konsern.svg";
import nita from "@/assets/img/nita.svg";

import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation, Pagination } from "swiper/modules";
import "swiper/css";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Navigation, Pagination],
    };
  },
  data() {
    return {
      marqueeLogoOne: [azimut, elvis, glonass, almaz, skba, rsai, traced],
      marqueeLogoTwo: [navigator, aviasia, spbgut, sogaz, konsern, nita],
    };
  },
  methods: {
    swiperPrev() {
      document.querySelector(".swiper-button-prev").click();
      document.querySelector(
        ".swiper-navigation .swiper-pagination-current",
      ).innerHTML = document.querySelector(
        ".swiper-pagination-current",
      ).innerHTML;
    },
    swiperNext() {
      document.querySelector(".swiper-button-next").click();
      document.querySelector(
        ".swiper-navigation .swiper-pagination-current",
      ).innerHTML = document.querySelector(
        ".swiper-pagination-current",
      ).innerHTML;
    },
  },
  mounted() {
    document.querySelector(
      ".swiper-navigation .swiper-pagination-current",
    ).innerHTML = document.querySelector(
      ".swiper-pagination-current",
    ).innerHTML;
  },
};
</script>

<template>
  <div class="index-page">
    <section class="home">
      <div class="main-container">
        <div class="home-in">
          <h1 class="home-title">
            <span class="title-big">Рубикон</span>
            <span class="title-small"
              >Цифровая система контроля и защиты от БПЛА</span
            >
          </h1>
          <div class="home-bg">
            <img src="@/assets/img/home-bg.png" alt="" />
            <img src="@/assets/img/home-bg-planshet.png" alt="" />
          </div>
          <p class="home-description">
            Надежное решение <br />
            для обнаружения, контроля <br />
            и противодействия БПЛА, <br />
            а также обеспечение <br />
            безопасного применения <br />
            беспилотников <br />
            для предприятий и субъектов РФ
          </p>
        </div>
      </div>
    </section>
    <section id="products" class="products">
      <div class="main-container">
        <h2 class="section-title">Что мы предлагаем</h2>
        <div class="products-cards">
          <div class="card-item" v-for="item of 4" :key="item">
            <div class="card-body">
              <div class="card-title">Мониторинг и обработка информации</div>
              <ul class="card-description">
                <li>Идентификация по принципу «свой-чужой»</li>
                <li>Отображение уровня угроз</li>
                <li>Обеспечение оперативного предупреждения нарушений</li>
                <li>
                  Передача управляющих команд <br />
                  на оборудование РЭБ
                </li>
                <li>
                  Возможность купольного и секторального <br />
                  (направленного) подавления
                </li>
                <li>
                  Интеграции неограниченного количества <br />
                  оборудования РЭБ
                </li>
                <li>Контроль состояния комплексов оборудования</li>
              </ul>
            </div>
            <div class="card-img">
              <img
                src="@/assets/img/products-card-img.png"
                alt="product card img"
              />
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="workplace">
      <div class="main-container">
        <img
          src="@/assets/img/workplace-img.png"
          alt="workplace-img"
          class="workplace-img"
        />
        <span class="workplace-title">Пример рабочего места АРМ</span>
      </div>
    </section>
    <section class="logoMarqueeSection">
      <div class="container" id="logoMarqueeSection">
        <div class="default-content-container flex items-center">
          <div class="default-content-container-inner marquee-wrapper">
            <div class="marquee">
              <a target="_blank" v-for="(img, i) in marqueeLogoOne" :key="i"
                ><img
                  :src="img"
                  title=""
                  class="marqueelogo"
                  style="width: auto; max-width: none"
              /></a>
            </div>
            <div class="marquee">
              <a target="_blank" v-for="(img, i) in marqueeLogoOne" :key="i"
                ><img
                  :src="img"
                  title=""
                  class="marqueelogo"
                  style="width: auto; max-width: none"
              /></a>
            </div>
          </div>
          <div class="default-content-container-inner marquee-wrapper">
            <div class="marquee">
              <a target="_blank" v-for="(img, i) in marqueeLogoTwo" :key="i"
                ><img
                  :src="img"
                  title=""
                  class="marqueelogo"
                  style="width: auto; max-width: none"
              /></a>
            </div>
            <div class="marquee">
              <a target="_blank" v-for="(img, i) in marqueeLogoTwo" :key="i"
                ><img
                  :src="img"
                  title=""
                  class="marqueelogo"
                  style="width: auto; max-width: none"
              /></a>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section id="projects" class="projects">
      <div class="main-container">
        <h2 class="section-title">Проекты</h2>
        <div class="projects-swiper">
          <swiper
            :pagination="{
              type: 'fraction',
            }"
            :cssMode="true"
            :navigation="true"
            :modules="modules"
            :space-between="30"
            class="mySwiper"
          >
            <swiper-slide v-for="item of 23" :key="item">
              <div class="swiper-card">
                <div class="project-name">Проект «Анапа»</div>
                <div class="project-info">
                  <div class="project-img">
                    <img src="@/assets/img/project1.png" alt="" />
                  </div>
                  <p class="project-body">
                    Программно-аппаратный комплекс «Рубикон» стоит на защите
                    объекта топливно-энергетического комплекса. Объект оснащен
                    несколькими комплексами обнаружения и подавления БВС
                    различных производителей отечественного оборудования
                    «ROSC-1», производства ПАО «НПО «Алмаз», а также «Поляна» и
                    «Рубеж», производства АО «НПЦ «ЭЛВИС». В состав комплексов
                    обнаружения входят радиолокаци-онная станция (РЛС), системы
                    радиотехнической разведки (РТР), обзорные оптические и
                    оптико-электронные системы (ООС и ОЭС), средства
                    радиоэлектронного подавления (РЭП), а также оборудование
                    автоматического зависимого наблюдения (АЗН).
                  </p>
                </div>
                <div class="project-info">
                  <div class="project-img">
                    <img src="@/assets/img/project2.png" alt="" />
                  </div>
                  <p class="project-body">
                    ПАК «Рубикон» обеспечивает консолидацию, обработку и
                    отображение данных наблюдения за воздушным пространством от
                    всех доступных источников и предоставляет оператору
                    обобщённую информацию о ситуационной осведомленности в своей
                    зоне ответственности. <br /><br />
                    В том числе, на основании данных АЗН ПАК «Рубикон»
                    обеспечивает определение БВС по принципу «свой/чужой», что
                    позволяет исключить ошибочное подавление средствами РЭП БВС,
                    легально выполняющих полет. <br /><br />
                    ПАК «Рубикон» обеспечивает информационный вынос в адрес
                    Минобороны РФ.
                  </p>
                </div>
              </div>
            </swiper-slide>
          </swiper>
          <div class="projects-swiper-bottom">
            <div class="swiper-navigation">
              <div class="swiper-button-prev" @click="swiperPrev"></div>
              <div class="swiper-pagination">
                <span class="swiper-pagination-current">3</span> из
                <span class="swiper-pagination-total">23</span>
              </div>
              <div class="swiper-button-next" @click="swiperNext"></div>
            </div>
            <div class="view-all">
              <router-link to="#"> Смотреть все </router-link>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="team">
      <div class="main-container">
        <h2 class="section-title">Команда</h2>
        <div class="team-card">
          <div class="card-body">
            Команда проекта Рубикон - это команда высокого уровня профессионалов
            из авиационной и ИТ отрасли с опытом работы и реализации проектов
            "под ключ" более 20 лет.
          </div>
          <div class="team-img">
            <img src="" alt="" />
          </div>
        </div>
      </div>
    </section>
    <section id="contact" class="contact">
      <div class="main-container">
        <h2 class="section-title">Свяжитесь с нами</h2>
        <div class="contact-in">
          <div class="contact-form">
            <form>
              <div class="form-control">
                <input type="text" placeholder="Имя" class="" />
                <span class="error-text">Неверный формат ввода</span>
              </div>
              <div class="form-control">
                <input type="text" placeholder="Компания" />
                <span class="error-text">Неверный формат ввода</span>
              </div>
              <div class="form-control">
                <input type="text" placeholder="Телефон" />
                <span class="error-text">Неверный формат ввода</span>
              </div>
              <div class="form-control">
                <input type="email" placeholder="Почта" />
                <span class="error-text">Неверный формат ввода</span>
              </div>
              <button class="leave-request_btn">Оставить заявку</button>
            </form>
          </div>
          <div class="contact-img">
            <img src="@/assets/img/contact-img.svg" alt="" />
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style lang="scss">
.index-page {
  .home {
    position: relative;
    .main-container {
      position: relative;
    }
    &::before {
      content: "";
      width: 100%;
      height: 1035px;
      background-image: url("@/assets/img/home-bg-blur.png");
      background-repeat: no-repeat;
      background-size: 1280px;
      background-position: center -250px;
      position: absolute;
      top: -50px;
      left: 50%;
      transform: translateX(-50%);
    }
    .home-in {
      padding-top: 80px;
      position: relative;
      z-index: 2;
      display: flex;
      flex-wrap: wrap;
      align-items: start;
      .home-title {
        min-width: 321px;
        margin-top: 226px;
        .title-big {
          display: block;
          font-family: var(--font-family);
          font-weight: 700;
          font-size: 64px;
          color: var(--white);
        }
        .title-small {
          display: block;
          max-width: 321px;
          font-family: var(--font-family);
          font-weight: 600;
          font-size: 20px;
          color: var(--white);
        }
      }
      .home-description {
        max-width: 827px;
        width: 100%;
        backdrop-filter: blur(5px);
        background: rgba(107, 109, 109, 0.2);
        border-radius: 16px;
        padding: 32px 208px 32px 32px;
        margin-top: -4px;
        font-family: var(--font-family);
        font-weight: 600;
        font-size: 32px;
        color: var(--white);
      }
      .home-bg {
        width: calc(100% - 321px);
        margin-top: -80px;
        position: sticky;
        top: 0;
        img {
          width: 100%;
          &:nth-child(2) {
            display: none;
          }
        }
      }
    }
  }
  .products {
    padding-top: 112px;
    position: relative;
    .products-cards {
      display: flex;
      flex-direction: column;

      gap: 32px;
      .card-item {
        display: flex;
        align-items: center;
        gap: 8px;
        .card-body {
          flex: 1 1 0;
          .card-title {
            font-family: var(--font-family);
            font-weight: 600;
            font-size: 24px;
            color: var(--white);
            margin-bottom: 4px;
          }
          .card-description {
            padding-left: 26px;
            font-family: var(--font-family);
            font-weight: 400;
            font-size: 16px;
            line-height: 20px;
            color: #fff;
          }
        }
        .card-img {
          flex: 1 1 0;
          img {
            width: 100%;
          }
        }
      }
    }
  }
  .workplace {
    padding-top: 112px;
    border-radius: 16px;
    .main-container {
      position: relative;
    }
    .workplace-img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    .workplace-title {
      position: absolute;
      left: 64px;
      bottom: 32px;
      z-index: 2;
      font-family: var(--font-family);
      font-weight: 600;
      font-size: 32px;
      color: var(--white);
    }
  }
  .logoMarqueeSection {
    overflow: hidden;
    .container {
      padding-top: 112px;
      .default-content-container {
        &:hover {
          .marquee {
            animation-play-state: paused !important;
          }
        }
      }
    }
    .marquee-wrapper {
      display: flex;
      justify-content: end;

      &:nth-child(1) {
        margin-bottom: 16px;
      }
      &:nth-child(2) {
        .marquee {
          animation-duration: 25.7s;
        }
      }
      .marquee {
        display: inline-flex;
        gap: 16px;
        margin: 0 8px;
        white-space: nowrap;
        position: relative;
        animation-name: marquee;
        animation-duration: 30s;
        animation-timing-function: linear;
        animation-iteration-count: infinite;

        a {
          width: 414px;
          height: 136px;
          display: inline-flex;
          align-items: center;
          justify-content: center;
          white-space: nowrap;
          background: rgba(107, 109, 109, 0.2);
          border-radius: 16px;
          backdrop-filter: blur(12px);
          cursor: pointer;
          transition: 0.3s;
          &:hover {
            background-color: var(--gray-dark);
          }
        }
      }
      @keyframes marquee {
        0% {
          transform: translate3d(0%, 0, 0);
        }
        100% {
          transform: translate3d(100%, 0, 0);
        }
      }
    }
  }
  .projects {
    padding-top: 112px;
    .projects-swiper {
      background: rgba(107, 109, 109, 0.3);
      border-radius: 24px;
      padding: 32px;
      overflow: hidden;
      .swiper-slide {
        .swiper-card {
          .project-name {
            font-family: var(--font-family);
            font-weight: 600;
            font-size: 24px;
            text-align: center;
            color: var(--white);
            margin-bottom: 32px;
          }
          .project-info {
            display: flex;
            align-items: center;
            gap: 32px;
            margin-bottom: 38px;
            &:last-child {
              margin-bottom: 0;
            }
            .project-body {
              font-family: var(--font-family);
              font-weight: 400;
              font-size: 16px;
              line-height: 21.6px;
              color: #fff;
            }
          }
        }
      }
      .swiper-button-prev,
      .swiper-button-next,
      .swiper-pagination {
        display: none;
      }
      .projects-swiper-bottom {
        max-width: 540px;
        width: 100%;
        float: right;
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-top: 60px;
        .swiper-navigation {
          display: flex;
          align-items: center;
          gap: 8px;
          .swiper-button-prev,
          .swiper-button-next {
            display: block !important;
          }
          .swiper-pagination {
            display: flex !important;
            gap: 4px;
          }
        }
        .view-all {
          a {
            font-family: var(--font-family);
            font-weight: 600;
            font-size: 16px;
            line-height: 20px;
            text-decoration: underline;
            text-decoration-skip-ink: none;
            color: #fff;
            transition: 0.3s;
            &:hover {
              color: var(--violet);
            }
          }
        }
      }
    }
  }
  .team {
    padding-top: 124px;
    .team-card {
      display: flex;
      align-items: center;
      gap: 56px;
      backdrop-filter: blur(12px);
      background: rgba(107, 109, 109, 0.2);
      border-radius: 16px;
      padding: 32px;
      .card-body {
        font-family: var(--font-family);
        font-weight: 600;
        font-size: 32px;
        color: var(--white);
      }
      .team-img {
        border-radius: 16px;
        min-width: 407px;
        height: 407px;
        background: #d9d9d9;
      }
    }
  }
  .contact {
    padding: 112px 0;
    .contact-in {
      position: relative;
      .contact-form {
        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 30px;
        backdrop-filter: blur(5px);
        background: rgba(107, 109, 109, 0.2);
        border-radius: 24px;
        padding: 32px;
        form {
          max-width: 568px;
          width: 100%;
          display: flex;
          flex-direction: column;
          gap: 32px;
        }
        .form-control {
          position: relative;
          input {
            width: 100%;
            background: var(--gray-light);
            border-radius: 8px;
            padding: 14px 16px;
            font-family: var(--font-family);
            font-weight: 600;
            font-size: 16px;
            line-height: 20px;
            color: var(--white);
            border: 2px solid transparent;
            &:focus {
              outline: none;
              border: 2px solid var(--white);
              background: var(--black);
            }

            &::placeholder {
              font-family: var(--font-family);
              font-weight: 600;
              font-size: 16px;
              color: var(--white);
            }
          }
          input.error {
            border: 2px solid #c00;
            background: var(--black);
          }
          .error-text {
            display: none;
            position: absolute;
            top: 100%;
            left: 16px;
            font-family: var(--font-family);
            font-weight: 600;
            font-size: 12px;
            color: #c00;
          }
          .error {
            display: block;
          }
        }
        .leave-request_btn {
          width: 100%;
          background: var(--blue);
          border-radius: 8px;
          padding: 14px;
          border: 0;
          font-family: var(--font-family);
          font-weight: 600;
          font-size: 16px;
          color: var(--white);
          cursor: pointer;
          transition: 0.3s;
          &:hover {
            background: var(--governor-bay-500);
          }
          &:active {
            background: var(--governor-bay-400);
          }
        }
      }
      .contact-img {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        right: 32px;
        z-index: -2;
      }
    }
  }
  // media
  @media (max-width: 992px) {
    .home {
      .home-in {
        align-items: stretch;
        .home-title {
          display: flex;
          flex-direction: column;
          justify-content: center;
          margin-top: 0;
          min-height: 100%;
        }
        .home-bg {
          img {
            &:nth-child(1) {
              display: none;
            }
            &:nth-child(2) {
              display: block;
            }
          }
        }
        .home-description {
          max-width: 582px;
          padding: 32px;
          font-size: 24px;
          br {
            display: none;
          }
        }
      }
    }
    .products {
      padding-top: 92px;
      .products-cards {
        gap: 24px;
        .card-item {
          align-items: start;
          .card-body {
            .card-title {
              font-size: 20px;
              margin-bottom: 4px;
            }
            .card-description {
              font-size: 12px;
              line-height: 16px;
            }
          }
        }
      }
    }
    .workplace {
      padding-top: 142px;
      .workplace-title {
        font-size: 24px;
        left: 48px;
        bottom: 3px;
      }
    }
    .logoMarqueeSection {
      .container {
        padding-top: 120px;
      }
      .marquee-wrapper {
        margin-bottom: 16px;
        &:last-child {
          margin-bottom: 0;
        }
        &:nth-child(1) {
          a {
            &:nth-child(1) {
              img {
                height: 50px;
              }
            }
            &:nth-child(2) {
              img {
                height: 42px;
              }
            }
            &:nth-child(3) {
              img {
                height: 41px;
              }
            }
            &:nth-child(4) {
              img {
                height: 96.75px;
              }
            }
            &:nth-child(5) {
              img {
                height: 60px;
              }
            }
            &:nth-child(6) {
              img {
                height: 84px;
              }
            }
            &:nth-child(7) {
              img {
                height: 84px;
              }
            }
          }
        }
        &:nth-child(2) {
          a {
            &:nth-child(1) {
              img {
                height: 46.5px;
              }
            }
            &:nth-child(2) {
              img {
                height: 45.75px;
              }
            }
            &:nth-child(3) {
              img {
                height: 58.5px;
              }
            }
            &:nth-child(4) {
              img {
                height: 84px;
              }
            }
            &:nth-child(5) {
              img {
                height: 84px;
              }
            }
            &:nth-child(6) {
              img {
                height: 84px;
              }
            }
          }
        }
        .marquee {
          a {
            width: 311px;
            height: 102px;
          }
        }
      }
    }
    .projects {
      padding-top: 92px;
      .projects-swiper {
        .swiper-slide {
          .swiper-card {
            .project-name {
              margin-bottom: 24px;
            }
            .project-info {
              margin-bottom: 24px;
              gap: 16px;
              &:last-child {
                margin-bottom: 0;
              }
              .project-body {
                font-size: 12px;
                line-height: 16px;
                text-overflow: ellipsis;
                overflow: hidden;
                display: -webkit-box;
                -webkit-line-clamp: 15;
                -webkit-box-orient: vertical;
              }
              .project-img {
                min-width: calc(50% + 38px);
                img {
                  width: 100%;
                }
              }
            }
          }
        }
        .projects-swiper-bottom {
          max-width: calc(50% + 45px);
          margin-top: 32px;
        }
      }
    }
    .team {
      padding-top: 92px;
      .team-card {
        gap: 16px;
        .card-body {
          font-size: 24px;
        }
        .team-img {
          min-width: 268px;
          height: 268px;
        }
      }
    }
    .contact {
      padding-top: 92px;
      .contact-in {
        .contact-form {
          form {
            max-width: 100%;
          }
        }
        .contact-img {
          width: calc(100% - 2px);
          overflow: hidden;
          display: flex;
          justify-content: center;
          left: 50%;
          top: 50%;
          transform: translate(-50%, -50%);
        }
      }
    }
  }
  @media (max-width: 650px) {
    .home {
      .home-in {
        padding-top: 93px;
        flex-direction: column;
        .home-title {
          align-items: center;
          text-align: center;
        }
        .home-bg {
          width: calc(100% + 32px);
          margin-top: -171px;
          margin-left: -16px;
        }
        .home-description {
          margin-top: 0;
        }
      }
    }
    .products {
      .products-cards {
        .card-item {
          flex-direction: column;
          .card-body {
            order: 2;
          }
          .card-img {
            order: 1;
          }
        }
      }
    }
    .projects {
      .projects-swiper {
        .swiper-slide {
          .swiper-card {
            .project-info {
              flex-direction: column;
              .project-img {
                width: 100%;
              }
              .project-body {
                -webkit-line-clamp: 20;
              }
            }
          }
        }
      }
    }
    .team {
      .team-card {
        flex-direction: column;
        .team-img {
          width: 100%;
        }
      }
    }
  }
  @media (max-width: 500px) {
    .home {
      &::before {
        top: -100px;
      }
      .home-in {
        .home-title {
          min-width: 100%;
          .title-big {
            font-size: 32px;
            margin-bottom: 8px;
          }
          .title-small {
            max-width: 263px;
            font-size: 16px;
          }
        }
        .home-bg {
          margin-top: -108px;
        }
        .home-description {
          font-weight: 600;
          font-size: 12px;
          text-align: center;
        }
      }
    }
    .products {
      padding-top: 64px;
      .products-cards {
        .card-item {
          gap: 16px;
          .card-body {
            .card-title {
              text-align: center;
            }
          }
          .card-img {
            order: 1;
          }
        }
      }
    }
    .workplace {
      padding-top: 64px;
      .workplace-img {
        border-radius: 8px;
      }
      .workplace-title {
        font-size: 12px;
        left: 24px;
        bottom: 8px;
      }
    }
    .logoMarqueeSection {
      .container {
        padding-top: 64px;
      }
      .marquee-wrapper {
        &:nth-child(1) {
          a {
            &:nth-child(1) {
              img {
                height: 35px;
              }
            }
            &:nth-child(2) {
              img {
                height: 29.4px;
              }
            }
            &:nth-child(3) {
              img {
                height: 28.7px;
              }
            }
            &:nth-child(4) {
              img {
                height: 67.725px;
              }
            }
            &:nth-child(5) {
              img {
                height: 42px;
              }
            }
            &:nth-child(6) {
              img {
                height: 58.8px;
              }
            }
            &:nth-child(7) {
              img {
                height: 58.8px;
              }
            }
          }
        }
        &:nth-child(2) {
          a {
            &:nth-child(1) {
              img {
                height: 32.55px;
              }
            }
            &:nth-child(2) {
              img {
                height: 32.025px;
              }
            }
            &:nth-child(3) {
              img {
                height: 40.95px;
              }
            }
            &:nth-child(4) {
              img {
                height: 58.8px;
              }
            }
            &:nth-child(5) {
              img {
                height: 58.8px;
              }
            }
            &:nth-child(6) {
              img {
                height: 58.8px;
              }
            }
          }
        }
        .marquee {
          a {
            width: 217.7px;
            height: 71.4px;
          }
        }
      }
    }
    .projects {
      padding-top: 64px;
      .main-container {
        padding: 0;
      }
      .projects-swiper {
        padding: 16px;
        .projects-swiper-bottom {
          max-width: 100%;
          flex-direction: column;
          margin-top: 16px;
          gap: 8px;
          .view-all {
            a {
              font-size: 14px;
              line-height: 16px;
            }
          }
        }
      }
    }
    .team {
      padding-top: 64px;
      .team-card {
        padding: 16px;
        .card-body {
          font-size: 18px;
          font-weight: 500;
        }
        .team-img {
          width: 100%;
        }
      }
    }
    .contact {
      padding: 64px 0;
      .contact-in {
        .contact-form {
          padding: 32px 16px;
          form {
            gap: 16px;
          }
        }
        .contact-img {
          img {
            max-height: 322px;
          }
        }
      }
    }
  }
}
</style>
