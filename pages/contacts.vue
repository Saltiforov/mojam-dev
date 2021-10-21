<template>
  <main>
    <section id="contacts">
      <div class="container">
        <div class="contacts">
          <p class="contacts__crumbs">
            {{ crumbsActive }} <span>{{ crumbs }}</span>
          </p>
          <div class="contacts__info">
            <h2 class="contacts__info-title">
              {{ title }}
            </h2>
            <div class="contacts__info-map contacts__map">
              <div id="map"></div>
              <div class="contacts__map-modal map__modal">
                <h2 class="map__modal-title">
                  {{ modal.title }}
                </h2>
                <p class="map__modal-subtitle">
                  {{ modal.subtitle }}
                </p>
                <div class="map__modal-content">
                  <input type="text" placeholder="Имя и фамилия" />
                  <input type="text" placeholder="Емейл" />
                  <textarea placeholder="Ваш комментарий" />
                </div>
                <button class="map__modal-btn">Отправить</button>
              </div>
              <div class="contacts__map-info map__contacts">
                <div class="map__contacts-logo">
                  <img
                    src="/logo-black.svg"
                    alt="logo"
                    class="footer__logo-img"
                  />
                </div>
                <div class="map__contacts-info">
                  <p>{{ contacts.city }}</p>
                  <p><img src="/phone.svg" alt="mail" />{{ contacts.phone }}</p>
                  <p>{{ contacts.address }}</p>
                  <p><img src="/mail.svg" alt="phone" />{{ contacts.mail }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: "contacts",
  data() {
    return {
      crumbsActive: "Главная /",
      crumbs: "Истории",
      title: "Контакты",
      modal: {
        title: "Напишите нам",
        subtitle: "И мы обязательно ответим"
      },
      contacts: {
        city: "Харьков, Украина",
        address: "Мироносицкая 15, этаж 4, офис 404",
        phone: "+38 050 769 30 61",
        mail: "company@mojam.co"
      }
    };
  }
};
</script>

<style lang="scss">
.contacts {
  padding: 14.6rem 0 6rem 0;

  &__crumbs {
    position: absolute;
    color: $grey;
    font-size: 1rem;
    line-height: 2rem;
    top: 11rem;

    span {
      color: $lightGrey;
    }
  }

  &__info {
    &-title {
      font-size: 3rem;
      line-height: 3.4rem;
      position: relative;
      margin-bottom: 5.3rem;
      margin-left: 10rem;

      &::after {
        content: "";
        position: absolute;
        top: 3.8rem;
        right: 0;
        left: 0;
        bottom: 0;
        width: 10rem;
        height: 0.2rem;
        background: $green;
      }
    }

    &-map {
      background-color: #b5b5b5;
      width: 100%;
      max-height: 52rem;
      padding: 6rem 0 4rem;
      display: flex;
      justify-content: space-between;
    }
  }
}

.map__modal {
  width: 28rem;
  height: 42rem;
  background: rgba(254, 254, 254, 0.9);
  box-shadow: 0 0.4rem 0.4rem rgba(0, 0, 0, 0.05);
  border-radius: 1rem;
  margin-left: 6rem;
  padding: 0 3rem 0 2.8rem;
  box-sizing: border-box;

  &-title {
    font-size: 2rem;
    line-height: 2.3rem;
    position: relative;
    padding: 2.6rem 0 2.2rem;

    &::after {
      content: "";
      position: absolute;
      top: 5.5rem;
      right: 0;
      left: 0;
      bottom: 0;
      width: 10rem;
      height: 0.2rem;
      background: $green;
    }
  }

  &-subtitle {
    font-size: 1.4rem;
    line-height: 1.6rem;
    display: flex;
    justify-content: flex-end;
    letter-spacing: 0;
    padding-bottom: 1.7rem;
  }

  &-content {
    input,
    textarea {
      font-family: GillLight, sans-serif;
      background: rgba(29, 29, 29, 0.02);
      border: 1px solid #0e0e0e;
      padding: 1rem 1.3rem;
      width: 100%;
      box-sizing: border-box;
      font-size: 1.2rem;
      line-height: 1.4rem;
      color: rgba(14, 14, 14, 0.5);
    }

    input {
      &:nth-child(2) {
        margin: 2rem 0;
      }
    }
  }

  textarea {
    height: 9rem;
    margin-bottom: 3.6rem;
  }

  &-btn {
    color: white;
    background: linear-gradient(92.63deg, #ff9c40 0%, #edc951 100%);
    border-radius: 5px;
    padding: 1.1rem 5.4rem;
    border: none;
    display: block;
    margin: 0 auto 4rem;
    cursor: pointer;
  }
}

.map__contacts {
  width: 43rem;
  height: 18rem;
  background: rgba(254, 254, 254, 0.9);
  box-shadow: 0 0.4rem 0.4rem rgba(0, 0, 0, 0.05);
  border-radius: 10px;
  align-self: flex-end;
  margin-right: 11.4rem;
  padding: 3rem;
  box-sizing: border-box;
  &-info {
    display: grid;
    grid-template-columns: 11rem 15rem;
    gap: 0.9rem 6.6rem;
    padding-top: 2.5rem;
    align-items: flex-start;
    p {
      display: flex;
      font-size: 1.4rem;
      line-height: 1.6rem;
      letter-spacing: 0;
      font-weight: 300;
      &:nth-child(2) {
        position: relative;
        top: -0.5rem;
      }
    }
    img {
      padding-right: 1.4rem;
    }
  }
}

@media screen and (max-width: 460px) {
  .contacts {
    padding: 45.8rem 0 20.5rem 0;
    &__crumbs {
      display: none;
    }
    &__info {
      &-title {
        font-size: 9.6rem;
        line-height: 11.2rem;
        position: relative;
        margin-bottom: 21rem;
        margin-left: 0;
        &:after {
          content: "";
          position: absolute;
          top: 12rem;
          right: 0;
          left: 0;
          bottom: 0;
          width: 40rem;
          height: 1rem;
          background: #41b7a8;
        }
      }
      &-map {
        flex-direction: column-reverse;
        background: none;
        position: relative;
        max-height: 100%;
        padding-top: 107rem;
      }
    }
  }
  #map {
    position: absolute;
    top: 0;
    left: -8rem;
    z-index: 0;
    width: 144rem;
    height: 177.2rem;
    background: gray;
  }
  .map {
    &__modal {
      position: relative;
      z-index: 2;
      width: 100%;
      height: 141.6rem;
      margin: 0;
      padding: 0;
      &-title {
        font-size: 8rem;
        line-height: 11.2rem;
        position: relative;
        margin-bottom: 7.5rem;
        margin-left: 0;
        padding: 0;
        &:after {
          content: "";
          position: absolute;
          top: 12rem;
          right: 0;
          left: 0;
          bottom: 0;
          width: 40rem;
          height: 1rem;
          background: #41b7a8;
        }
      }
      &-subtitle {
        justify-content: flex-start;
        font-size: 5.6rem;
        line-height: 6.4rem;
        padding-bottom: 6.8rem;
      }
      &-content {
        width: 88.8rem;
        margin: 0 auto;
        input,
        textarea {
          padding: 4rem 5.3rem;
          font-size: 4.8rem;
          line-height: 5.6rem;
        }
        input:nth-child(2) {
          margin: 8rem 0;
        }
        textarea {
          height: 36rem;
          margin-bottom: 15rem;
        }
      }
      &-btn {
        font-size: 4.8rem;
        line-height: 5.6rem;
        padding: 4.5rem 22.6rem;
      }
    }
    &__contacts {
      position: relative;
      z-index: 2;
      margin: 0;
      width: 100%;
      height: 62.8rem;
      padding: 7rem;
      display: flex;
      flex-direction: row-reverse;
      justify-content: space-between;
      align-self: center;
      margin-bottom: 30rem;
      &-logo {
        img {
          width: 34rem;
          position: relative;
          top: 1rem;
          right: 1rem;
        }
      }
      &-info {
        grid-template-columns: 58.2rem;
        gap: 3.5rem;
        padding: 0;
        img {
          padding-right: 6rem;
        }
        p {
          font-size: 5.6rem;
          line-height: 6.4rem;
          &:nth-child(1) {
            order: 1;
          }
          &:nth-child(2) {
            order: 3;
          }
          &:nth-child(3) {
            order: 2;
            width: 50rem;
          }
          &:nth-child(4) {
            order: 4;
          }
        }
      }
    }
  }
}
</style>
