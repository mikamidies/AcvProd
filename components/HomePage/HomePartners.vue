<template>
  <div class="wrap">
    <div class="anchor" id="partners"></div>
    <div class="container">
      <h4 class="title">Bizning mijozlarimiz</h4>
      <div class="swiper" ref="studSwiper">
        <div class="swiper-wrapper">
          <div class="swiper-slide" v-for="item in partners" :key="item.id">
            <p class="name">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="20"
                height="20"
                viewBox="0 0 20 20"
                fill="none"
              >
                <path
                  d="M9.73314 0.237062C9.77067 -0.0790205 10.2293 -0.0790205 10.2669 0.237062L10.5815 2.8887C10.9878 6.31269 13.6873 9.01224 17.1113 9.41851L19.7629 9.73314C20.079 9.77067 20.079 10.2293 19.7629 10.2669L17.1113 10.5815C13.6873 10.9878 10.9878 13.6873 10.5815 17.1113L10.2669 19.7629C10.2293 20.079 9.77067 20.079 9.73314 19.7629L9.41851 17.1113C9.01224 13.6873 6.31269 10.9878 2.8887 10.5815L0.237062 10.2669C-0.0790205 10.2293 -0.0790205 9.77067 0.237062 9.73314L2.8887 9.41851C6.31269 9.01224 9.01224 6.31269 9.41851 2.8887L9.73314 0.237062Z"
                  fill="#A8C6DC"
                />
              </svg>
              {{ item.name }}
            </p>

            <img :src="item.img" alt="" class="pic" />

            <p class="status">
              {{ item.status }}
            </p>

            <a :href="item.link" target="_blank" class="link">
              Batafsil
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
              >
                <path
                  d="M14 8L18 12M18 12L14 16M18 12L6 12"
                  stroke="#1890ff"
                  stroke-width="1.5"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </a>
          </div>
          <div class="swiper-slide last">
            <p class="txt">yana</p>
            <p class="num">20+</p>
            <p class="txt">ortiq mijozlar</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Swiper from "swiper/swiper-bundle.js";
import "swiper/swiper-bundle.min.css";

export default {
  data() {
    return {
      partners: [
        {
          id: 0,
          name: "Barno Dilshodovna",
          status: "8 yillik tajriba vinirlari",
          img: "/images/1.jpg",
          link: "https://www.instagram.com/doctor_barno_dilshodovna/",
        },
        {
          id: 1,
          name: "Azimov Izzat",
          status: "💈 12 yillik soch va soqol bo’yicha tajriba",
          img: "/images/2.jpg",
          link: "https://www.instagram.com/azimov__izzat/",
        },
        {
          id: 2,
          name: "365 Travel",
          status: "🌍 365 kun dunyo bo'ylab sayohatda bo'ling!",
          img: "/images/3.jpg",
          link: "https://www.instagram.com/365travel.uz/",
        },
        {
          id: 3,
          name: "Bella Vita",
          status: "Свадебные Платья | Ателье ",
          img: "/images/4.jpg",
          link: "https://www.instagram.com/bellavita_wedding/",
        },
        {
          id: 4,
          name: "Abdurasulov Travel",
          status: "Allohni eng go’zal manzil makonlarida ko’rishguncha",
          img: "/images/5.jpg",
          link: "https://www.instagram.com/abdurasulov_travel/",
        },
        {
          id: 5,
          name: "Zilola Design",
          status: "Dizayn sohasida mutaxassis",
          img: "/images/6.jpg",
          link: "https://www.instagram.com/zilola_design/",
        },
        {
          id: 6,
          name: "Gulomov Invest",
          status: "🏢 futureinvest.uz asoschisi",
          img: "/images/7.jpg",
          link: "https://www.instagram.com/gulomov_invest/",
        },
        {
          id: 7,
          name: "Abror Azamov",
          status: "SMM | Marketolog 📈",
          img: "/images/8.jpg",
          link: "https://www.instagram.com/azamovv_abror?igsh=ZWwxem1wajhuNzRl",
        },
        {
          id: 8,
          name: "Dilbar Zakirova",
          status: "🏢 Основатель Bellavita Wedding и Bellavita Dantel",
          img: "/images/9.jpg",
          link: "https://www.instagram.com/dilbarzakirova_/",
        },
      ],
    };
  },

  mounted() {
    new Swiper(this.$refs.studSwiper, {
      slidesPerView: 1.5,
      spaceBetween: 8,
      breakpoints: {
        1024: {
          slidesPerView: 4,
          spaceBetween: 16,
        },
      },
      autoplay: {
        delay: 3000,
        disableOnInteraction: false,
      },
    });
  },
};
</script>

<style scoped>
.wrap {
  padding-bottom: 120px;
  position: relative;
  overflow: hidden;
}
.grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 4px;
  max-width: 80%;
  margin: 0 auto;
}
.title {
  text-align: center;
  margin-bottom: 24px;
}
.swiper {
  overflow: visible;
}
.swiper-slide {
  border: 1px solid var(--grey-8, #ebebeb);
  background: var(--White, #fff);
  padding: 28px 24px;
  transition: 0.4s;
}
.swiper-slide:hover {
  box-shadow: 0px 8px 24px 0px rgba(0, 25, 53, 0.16);
}
.name {
  font-family: var(--decor);
  color: var(--Blue-night, #001935);
  font-size: 20px;
  font-style: normal;
  font-weight: 500;
  line-height: 140%; /* 28px */
  margin-bottom: 22px;
  display: flex;
  align-items: center;
  gap: 8px;
}
.pic {
  width: 100%;
  height: 349px;
  object-fit: cover;
  margin-bottom: 24px;
}
.status {
  color: var(--grey-80, #353437);
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 140%; /* 22.4px */
  height: 45px;
}
.link {
  display: flex;
  align-items: center;
  gap: 8px;
  margin-top: 12px;
}
.last {
  background: var(--blue);
  color: white;
  height: auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 24px;
  text-align: center;
}
.txt {
  line-height: 100%;
  font-size: 24px;
  transition: 0.3s;
}
.num {
  font-size: 56px;
  font-family: var(--decor);
  line-height: 100%;
  transition: 0.3s;
}
.swiper-slide:hover .txt,
.swiper-slide:hover .num {
  transform: scale(1.1);
}
@media screen and (max-width: 1024px) {
  .wrap {
    padding-bottom: 80px;
  }
  .swiper-slide {
    padding: 16px;
  }
  .name {
    font-size: 16px;
    margin-bottom: 16px;
  }
  .pic {
    height: 230px;
    margin-bottom: 16px;
  }
  .status {
    font-size: 14px;
  }
}
</style>
