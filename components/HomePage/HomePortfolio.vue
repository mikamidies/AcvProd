<template>
  <div class="wrap">
    <h1 class="title">Portfolio</h1>
    <div class="items">
      <div
        class="item"
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
export default {
  data() {
    return {
      modalHandle: false,
      videosOne: {},
      videos: [
        {
          src: "DmWWqogr_r8",
          id: 0,
        },
        {
          src: "qFLhGq0060w",
          id: 1,
        },
        {
          src: "v3L1XdqGnyI",
          id: 2,
        },
        {
          src: "HmAsUQEFYGI",
          id: 3,
        },
      ],
    };
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
}
.wrap {
  padding: 40px 0;
}
.items {
  padding: 40px 24px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
.item {
  padding: 12px;
  height: 440px;
  cursor: pointer;
  transition: 0.4s;
}
.item:hover {
  background: #ebebeb;
}
.item:nth-child(2) {
  margin-top: 40px;
}
.item:nth-child(4),
.item:nth-child(6) {
  margin-top: -40px;
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
</style>
