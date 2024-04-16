<template>
  <div class="wrap" id="navbar">
    <div class="container">
      <div class="brand" @click="scrollElement('hero')">
        <img src="@/assets/img/white.png" alt="" />
      </div>
      <div class="burger">
        <div class="stick"></div>
      </div>
      <div class="links">
        <button @click="scrollElement('about')">Biz haqimizda</button>
        <button @click="scrollElement('portfolio')">Portfolio</button>
        <button @click="scrollElement('contacts')">Bog'lanish</button>
        <button @click="scrollElement('partners')">Hmakorlarimiz</button>
      </div>
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
  padding: 24px 0;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 999;
  transition: 0.4s;
}
.container {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
button {
  color: white;
  font-size: 18px;
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
.burger {
  display: none;
}
@media screen and (max-width: 1024px) {
  .links {
    position: fixed;
    top: 106px;
    left: 0;
    width: 100%;
    height: 100%;
    transform: translateX(-100%);
  }
  img {
    width: 120px;
  }
  .scroll img {
    width: 120px;
  }
  .burger {
    display: flex;
  }
  .stick {
    position: relative;
    width: 30px;
    height: 2px;
    background: white;
  }
  .stick::after {
    width: 30px;
    height: 2px;
    background: white;
    content: "";
    position: absolute;
    top: 10px;
    left: 0;
  }
  .stick::before {
    width: 30px;
    height: 2px;
    background: white;
    content: "";
    position: absolute;
    top: -10px;
    left: 0;
  }
}
</style>
