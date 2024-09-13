<script>
export default {
  data() {
    return {
      modal: false,
    };
  },
  methods: {
    modalMenu() {
      if (window.innerWidth < 992) {
        this.modal = !this.modal;
        if (this.modal) {
          document
            .querySelector("html")
            .style.setProperty("overflow", "hidden");
        } else {
          document
            .querySelector("html")
            .style.setProperty("overflow", "visible");
        }
      }
    },
  },
};
</script>
<template>
  <div class="header" :class="modal ? 'active' : ''">
    <div class="main-container">
      <div class="header-in">
        <div class="logo">
          <a href="#">
            <img src="@/assets/img/logo.svg" alt="logo" />
          </a>
        </div>
        <nav class="header-nav__bar">
          <div class="nav-link" :class="modal ? 'active' : ''">
            <div class="head">Меню</div>
            <a href="#products" class="nav-link__item" @click="modalMenu">
              Продукция
            </a>
            <a href="#projects" class="nav-link__item" @click="modalMenu">
              Проекты
            </a>
            <a href="#contact" class="nav-link__item" @click="modalMenu">
              Контакты
            </a>
          </div>
          <div class="header-contact">
            <div class="email">
              <a href="mailto:info@flydrone.ru">
                <img src="@/assets/img/icons/message.svg" alt="email icon" />
                <span>info@flydrone.ru</span>
              </a>
            </div>
            <div class="phone">
              <a href="tel:+77777777777">
                <img src="@/assets/img/icons/phone.svg" alt="phone icon" />
              </a>
            </div>
          </div>
          <button class="burger-btn" @click="modalMenu">
            <img src="@/assets/img/burger.svg" alt="" />
          </button>
        </nav>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.header {
  width: 100%;
  padding: 8px 0;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 100;
  .header-in {
    display: flex;
    align-items: center;
    justify-content: space-between;
    .header-nav__bar {
      display: flex;
      align-items: center;
      .nav-link {
        display: flex;
        align-items: center;
        .head {
          display: none;
          font-family: var(--font-family);
          font-weight: 700;
          font-size: 64px;
          line-height: 78px;
          color: var(--white);
        }
        &__item {
          display: block;
          backdrop-filter: blur(12px);
          background: rgba(13, 15, 16, 0.2);
          border-radius: 8px;
          padding: 8px 24px;
          user-select: none;
          font-family: var(--font-family);
          font-weight: 400;
          font-size: 16px;
          line-height: 20px;
          color: var(--white);
          transition: 0.3s;
          &:hover {
            background: rgba(182, 182, 182, 0.2);
          }
          &:active {
            background: rgba(255, 255, 255, 0.2);
          }
        }
      }
      .header-contact {
        display: flex;
        align-items: stretch;
        gap: 8px;
        .email,
        .phone {
          a {
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100%;
            background: var(--violet);
            border-radius: 8px;
            transition: 0.3s;
            &:hover {
              background-color: var(--gray-dark);
            }
          }
        }
        .email {
          a {
            gap: 10px;
            padding: 8px 16px;
            span {
              font-family: var(--font-family);
              font-weight: 400;
              font-size: 16px;
              line-height: 20px;
              color: var(--white);
            }
          }
        }
        .phone {
          a {
            padding: 0 10px;
          }
        }
      }
      .burger-btn {
        background: transparent;
        border: 0;
        display: none;
      }
    }
  }
}
@media (max-width: 992px) {
  .header {
    transition: 0.2s;
    .header-in {
      .logo {
        height: 48px;
        img {
          height: 48px;
        }
      }
      .header-nav__bar {
        gap: 16px;
        .nav-link {
          width: 100%;
          height: calc(100vh - 64px);
          background: var(--black);
          flex-direction: column;
          gap: 64px;
          padding: 32px;
          align-items: start;
          position: fixed;
          top: 100px;
          left: 0;
          opacity: 0;
          visibility: hidden;
          transition: 0.2s;
          .head {
            display: block;
          }
          .nav-link__item {
            padding: 0;
            font-weight: 700;
            font-size: 48px;
            line-height: 59px;
            color: var(--white);
            opacity: 0.3;
            &:hover {
              background: transparent;
            }
            &:active {
              background: transparent;
            }
            &:link {
              background: transparent;
            }
          }
        }
        .nav-link.active {
          top: 64px;
          opacity: 1;
          visibility: visible;
        }
        .header-contact {
          transition: 0.2s;
          .phone {
            display: none;
          }
        }
        .burger-btn {
          display: block;
        }
      }
    }
  }
  .header.active {
    background: var(--black);
    .header-in {
      .header-contact {
        visibility: hidden;
        opacity: 0;
      }
    }
  }
}
@media (max-width: 500px) {
  .header {
    .header-in {
      .logo {
        height: 32px;
        img {
          height: 32px;
        }
      }
      .header-nav__bar {
        .nav-link {
          height: calc(100vh - 48px);
          padding: 16px;
          gap: 48px;
          top: 80px;
          .head {
            font-size: 32px;
            line-height: 39px;
          }
          .nav-link__item {
            font-size: 32px;
            line-height: 39px;
          }
        }
        .nav-link.active {
          top: 48px;
        }
        .header-contact {
          display: none;
        }
        .burger-btn {
          height: 32px;
        }
      }
    }
  }
}
</style>
