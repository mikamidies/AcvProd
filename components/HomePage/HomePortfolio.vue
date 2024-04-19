<template>
  <div class="wrap">
    <div class="anchor" id="portfolio"></div>
    <div class="container">
      <h1 class="title">Portfolio</h1>
      <div class="swiper" ref="portSwiper">
        <div class="swiper-wrapper">
          <div
            class="item swiper-slide"
            v-for="item in videos"
            :key="item.id"
            @click="getId(item.id)"
          >
            <div class="iframe">
              <iframe
                :src="`https://www.youtube.com/embed/${item.src}?&controls=0&loop=1&rel=0&playlist=${item.src}`"
                title="YouTube video player"
                frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                referrerpolicy="strict-origin-when-cross-origin"
                allowfullscreen
              ></iframe>
            </div>
            <!-- <p class="name">
              {{ item.name }}
            </p> -->
          </div>
        </div>
      </div>
    </div>

    <div class="modal" :class="{ show: modalHandle }">
      <div class="space" @click="closeModal()"></div>
      <div class="x" @click="closeModal()">x</div>
      <div class="body">
        <iframe
          :src="`https://www.youtube.com/embed/${videosOne.src}?si=5i0LKoZy3JscQzaE`"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          referrerpolicy="strict-origin-when-cross-origin"
          allowfullscreen
        ></iframe>
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
      modalHandle: false,
      videosOne: {},
      videos: [
        { name: "Work Name", src: "QYHO8w4Y318", id: 0 },
        { name: "Work Name", src: "JhmsnAH8jK4", id: 1 },
        { name: "Work Name", src: "_cna4abVFus", id: 2 },
        { name: "Work Name", src: "tUAgcDFlZgc", id: 3 },
        { name: "Work Name", src: "3UsN6LPCfy4", id: 4 },
        { name: "Work Name", src: "KzDNv2B3UoE", id: 5 },
      ],
    };
  },

  mounted() {
    new Swiper(this.$refs.portSwiper, {
      slidesPerView: 1.3,
      spaceBetween: 16,
      autoplay: {
        delay: 3000,
      },
      breakpoints: {
        1024: {
          slidesPerView: 4,
        },
      },
      speed: 1000,
    });
  },

  methods: {
    getId(id) {
      this.videosOne = this.videos.find((item) => item.id == id);

      console.log(this.videosOne);

      this.openModal();
    },

    openModal() {
      this.modalHandle = true;
      document.body.style.overflow = "hidden";
    },
    closeModal() {
      this.modalHandle = false;
      document.body.style.overflow = "auto";

      this.videosOne = {};
    },
  },
};
</script>

<style scoped>
.title {
  text-align: center;
  font-weight: 600 !important;
  margin-bottom: 24px;
}
.wrap {
  padding: 0 0 80px 0;
  overflow: hidden;
}
.swiper {
  overflow: visible;
}
.items {
  padding: 40px 24px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
.item {
  padding: 12px;
  height: 620px;
  cursor: pointer;
  transition: 0.4s;
}
.item:hover {
  background: var(--blue);
}
.item:nth-child(even) {
  margin-top: 40px;
}
.iframe {
  width: 100%;
  height: 100%;
  overflow: hidden;
}
.iframe iframe {
  transform: scale(1.4);
  width: 100%;
  height: 100%;
  pointer-events: none;
}
.wrap {
  position: relative;
}
.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 999;
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  visibility: hidden;
  pointer-events: none;
  transition: 0.3s;
}
.modal.show {
  opacity: 1;
  visibility: visible;
  pointer-events: initial;
}
.space {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
}
.body {
  width: 60%;
  height: 70%;
  background: white;
  padding: 24px;
  position: relative;
  z-index: 2;
}
.body iframe {
  width: 100%;
  height: 100%;
}
.x {
  position: absolute;
  top: 32px;
  right: 32px;
  font-size: 32px;
  color: white;
  padding: 16px;
  cursor: pointer;
}
.name {
  font-size: 20px;
  font-weight: 500;
  margin-top: 24px;
  font-family: var(--regular-md);
}
@media screen and (max-width: 1024px) {
  .wrap {
    padding-bottom: 80px;
  }
  .item {
    height: 320px;
    padding: 0;
  }
  .item:nth-child(even) {
    margin-top: 24px;
  }
  .name {
    margin-top: 16px;
  }
  .body {
    width: 95%;
    height: 266px;
    padding: 8px;
  }
  .x {
    padding: 0;
  }
}
</style>
