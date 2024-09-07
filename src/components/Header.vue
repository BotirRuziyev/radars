<template>
  <div class="header">
    <div class="main-container">
      <div class="header-in">
        <div class="logo">
          <router-link to="/">
            <img src="@/assets/img/logo.svg" alt="logo" />
          </router-link>
        </div>
        <nav class="header-nav__bar">
          <div class="nav-link">
            <a href="#products" class="nav-link__item"> Продукция </a>
            <a href="#projects" class="nav-link__item"> Проекты </a>
            <a href="#contact" class="nav-link__item"> Контакты </a>
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
        &__item {
          display: block;
          backdrop-filter: blur(12px);
          background: rgba(13, 15, 16, 0.2);
          border-radius: 8px;
          padding: 8px 24px;
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
    }
  }
}
</style>
