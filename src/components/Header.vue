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
            <router-link to="#" class="nav-link__item"> Продукция </router-link>
            <router-link to="#" class="nav-link__item"> Проекты </router-link>
            <router-link to="#" class="nav-link__item"> Контакты </router-link>
          </div>
          <div class="header-contact">
            <div class="email">
              <router-link to="mail:info@flydrone.ru">
                <img src="@/assets/img/icons/message.svg" alt="email icon" />
                <span>info@flydrone.ru</span>
              </router-link>
            </div>
            <div class="phone">
              <router-link to="tel:+7">
                <img src="@/assets/img/icons/phone.svg" alt="phone icon" />
              </router-link>
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
            background-color: var(--gray-dark);
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
