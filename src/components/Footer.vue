<template>
  <footer class="footer">
    <div class="main-container">
      <div class="footer-in">
        <div class="left-block">
          <div class="logo">
            <router-link to="/">
              <img src="@/assets/img/logo.svg" alt="" />
              <span>Флай Дрон</span>
            </router-link>
          </div>
          <div class="footer-contact">
            <div class="label">Свяжитесь с нами</div>
            <a href="mailto:info@flydrone.ru" class="email-link"
              >info@flydrone.ru</a
            >
            <a href="#contact" class="telegram-link">
              <svg
                width="20"
                height="17"
                viewBox="0 0 20 17"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M1.38172 7.34613C6.74289 4.92692 10.3266 3.36329 12.1327 2.59622C17.2359 0.413036 18.2966 0.0295025 18.9847 0C19.128 0 19.4721 0.0295027 19.7014 0.206518C19.8734 0.35403 19.9308 0.560548 19.9595 0.708061C19.9881 0.855573 20.0168 1.1801 19.9881 1.44562C19.7014 4.42538 18.526 11.7125 17.8953 15.0463C17.6372 16.4624 17.1212 16.9344 16.6338 16.9935C15.573 17.082 14.7416 16.2559 13.7095 15.5773C12.1041 14.4857 11.1866 13.8072 9.60982 12.7451C7.80365 11.506 8.9791 10.8274 10.0112 9.73583C10.2692 9.44081 14.9997 5.04493 15.0857 4.6319C15.0857 4.57289 15.1143 4.39588 14.9997 4.30737C14.885 4.21886 14.7416 4.24836 14.627 4.27786C14.4549 4.30737 11.8747 6.07752 6.85756 9.55882C6.11216 10.0899 5.45277 10.3259 4.85071 10.3259C4.19132 10.3259 2.92986 9.94235 1.98378 9.61782C0.837002 9.23429 -0.0804165 9.02777 0.00559158 8.37872C0.0629303 8.05419 0.52164 7.70016 1.38172 7.34613Z"
                  fill="#191C1D"
                />
              </svg>
            </a>
          </div>
        </div>
        <div class="right-block">
          <div class="footer-contact">
            <div class="item">
              <div class="label">Телефон</div>
              <a href="tel:+77777777777" class="phone-link">
                +7 (777)-777-77-77
              </a>
            </div>
            <div class="item">
              <div class="item-in">
                <div class="label">Юр. адрес</div>
                <div class="location">Москва, Зоологическая улица, 26с2</div>
              </div>
              <div class="telegram-link-mobile">
                <a href="#contact" class="telegram-link">
                  <svg
                    width="17"
                    height="15"
                    viewBox="0 0 17 15"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      clip-rule="evenodd"
                      d="M1.30533 6.477C5.59426 4.54163 8.4612 3.29073 9.90613 2.67708C13.9886 0.930527 14.8373 0.6237 15.3877 0.600098C15.5024 0.600098 15.7776 0.6237 15.9611 0.765312C16.0987 0.883322 16.1446 1.04854 16.1675 1.16655C16.1905 1.28456 16.2134 1.54418 16.1905 1.7566C15.9611 4.1404 15.0207 9.9701 14.5162 12.6371C14.3097 13.77 13.8969 14.1477 13.507 14.1949C12.6584 14.2657 11.9933 13.6048 11.1676 13.062C9.88319 12.1887 9.14926 11.6458 7.88781 10.7962C6.44287 9.80488 7.38323 9.26204 8.20891 8.38876C8.41532 8.15274 12.1997 4.63604 12.2685 4.30561C12.2685 4.25841 12.2914 4.1168 12.1997 4.04599C12.1079 3.97519 11.9933 3.99879 11.9015 4.02239C11.7639 4.04599 9.69971 5.46211 5.686 8.24715C5.08968 8.67199 4.56216 8.8608 4.08052 8.8608C3.553 8.8608 2.54384 8.55398 1.78697 8.29435C0.869553 7.98753 0.135618 7.82231 0.204424 7.30307C0.250295 7.04345 0.617263 6.76022 1.30533 6.477Z"
                      fill="#191C1D"
                    />
                  </svg>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
.footer {
  background: var(--gray-dark);
  padding: 32px 0 85px;
  .footer-in {
    display: flex;
    justify-content: space-between;
    .label {
      font-family: var(--font-family);
      font-weight: 400;
      font-size: 16px;
      color: #f5f5f5;
      line-height: 20px;
      opacity: 0.4;
    }
    .left-block {
      .logo {
        margin-bottom: 32px;
        a {
          display: flex;
          align-items: center;
          gap: 16px;
          img {
            width: 48px;
            height: 48px;
          }
          span {
            font-family: var(--font-family);
            font-weight: 600;
            font-size: 32px;
            color: #fff;
          }
        }
      }
      .footer-contact {
        .email-link {
          display: block;
          font-family: var(--font-family);
          font-weight: 400;
          font-size: 24px;
          text-decoration: underline;
          text-decoration-skip-ink: none;
          color: #f5f5f5;
          margin-bottom: 16px;
          transition: 0.3s;
          &:hover {
            color: var(--governor-bay-700);
          }
          &:active {
            color: var(--governor-bay-500);
          }
        }
        .telegram-link {
          width: 30px;
          height: 30px;
          display: flex;
          align-items: center;
          padding-left: 4px;
          border-radius: 4px;
          background: var(--white);
          transition: 0.3s;
          &:hover {
            background: var(--governor-bay-700);
          }
          &:active {
            background: var(--governor-bay-500);
          }
        }
      }
    }
    .right-block {
      .footer-contact {
        display: flex;
        flex-direction: column;
        gap: 23px;
        .item {
          &:last-child {
            display: flex;
            justify-content: space-between;
            align-items: end;
            .telegram-link-mobile {
              display: none;
            }
          }
          .phone-link,
          .location {
            font-family: var(--font-family);
            font-weight: 400;
            font-size: 16px;
            color: #f5f5f5;
          }
          .phone-link {
            transition: 0.3s;
            &:hover {
              color: var(--governor-bay-700);
            }
            &:active {
              color: var(--governor-bay-500);
            }
          }
          .telegram-link {
            width: 24px;
            height: 24px;
            display: flex;
            align-items: center;
            border-radius: 4px;
            background: var(--white);
            padding-left: 3.2px;
            transition: 0.3s;
            &:hover {
              background: var(--governor-bay-700);
            }
            &:active {
              background: var(--governor-bay-500);
            }
          }
        }
      }
    }
  }
}
@media (max-width: 650px) {
  .footer {
    padding: 32px 0;
    .footer-in {
      flex-direction: column;
      gap: 25px;
      .left-block {
        .footer-contact {
          .telegram-link {
            display: none;
          }
        }
      }
      .right-block {
        .footer-contact {
          .item {
            &:last-child {
              gap: 20px;
              .telegram-link-mobile {
                display: block;
              }
            }
          }
        }
      }
    }
  }
}
@media (max-width: 500px) {
  .footer {
    padding: 16px 0;
    .footer-in {
      .label {
        font-size: 13px;
        line-height: 16px;
      }
      .left-block {
        .logo {
          margin-bottom: 16px;
          a {
            gap: 8px;
            img {
              width: 24px;
              height: 24px;
            }
            span {
              font-weight: 600;
              font-size: 16px;
            }
          }
        }
        .footer-contact {
          .email-link {
            font-size: 20px;
            line-height: 24px;
            margin-bottom: 0;
          }
        }
      }
      .right-block {
        .footer-contact {
          .item {
            .phone-link {
              font-size: 20px;
              line-height: 24px;
            }
          }
        }
      }
    }
  }
}
</style>
