<template>
  <div class="wrap" id="navbar">
    <div class="brand" @click="scrollElement('hero')">
      <img src="@/assets/img/white.png" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    scrollElement(id) {
      const element = document.getElementById(id);
      element.scrollIntoView({ block: "start", behavior: "smooth" });
    },
  },

  async mounted() {
    function scrollHeader() {
      const navbar = document.getElementById("navbar");
      if (this.scrollY >= 50) {
        navbar.classList.add("scroll");
      } else {
        navbar.classList.remove("scroll");
      }
    }
    window.addEventListener("scroll", scrollHeader);
  },
};
</script>

<style scoped>
.wrap {
  display: flex;
  justify-content: center;
  padding: 24px 0;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 999;
  transition: 0.4s;
}
.brand {
  display: flex;
  cursor: pointer;
}
img {
  width: 200px;
  object-fit: contain;
  transition: 0.3s;
}
.scroll {
  background: var(--black);
  padding: 12px 0;
  box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.2);
}
.scroll img {
  width: 180px;
}
</style>
