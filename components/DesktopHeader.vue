<template>
  <div class="wrap" id="navbar" :class="{ blacked: menuHandle == true }">
    <div class="container">
      <div class="brand" @click="scrollElement('hero')">
        <img src="@/assets/img/white.png" alt="" />
      </div>
      <div
        class="burger"
        @click="menuHandle = !menuHandle"
        :class="{ x: menuHandle == true }"
      >
        <div class="stick"></div>
      </div>
      <div class="links" :class="{ show: menuHandle == true }">
        <button @click="scrollElement('about'), (menuHandle = false)">
          Biz haqimizda
        </button>
        <button @click="scrollElement('portfolio'), (menuHandle = false)">
          Portfolio
        </button>
        <button @click="scrollElement('contacts'), (menuHandle = false)">
          Bog'lanish
        </button>
        <button @click="scrollElement('partners'), (menuHandle = false)">
          Mijozlarimiz
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      menuHandle: false,
    };
  },

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
  .wrap {
    position: relative;
    background: black;
  }
  .scroll {
    position: fixed;
  }
  .links {
    position: fixed;
    top: 85px;
    left: 0;
    width: 100%;
    height: 100%;
    transform: translateX(-100%);
    transition: 0.4s;

    background: black;
    display: flex;
    flex-direction: column;
    gap: 18px;
    padding: 32px 12px;
  }
  .links.show {
    transform: translateX(0);
  }
  .links button {
    font-size: 22px;
  }
  .scroll .links {
    top: 62px;
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
    transition: 0.3s;
  }
  .stick::after {
    width: 30px;
    height: 2px;
    background: white;
    content: "";
    position: absolute;
    top: 10px;
    left: 0;
    transition: 0.3s;
  }
  .stick::before {
    width: 30px;
    height: 2px;
    background: white;
    content: "";
    position: absolute;
    top: -10px;
    left: 0;
    transition: 0.3s;
  }
  .x .stick {
    transform: rotate(45deg);
  }
  .x .stick::after {
    transform: rotate(270deg);
    top: 0;
  }
  .x .stick::before {
    display: none;
  }
}
</style>
